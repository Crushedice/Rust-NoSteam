# Rust-NoSteam
Discord: sensais

## ⭐ » Donations
- https://qiwi.com/n/SENSAIS
- USDT Tether 0xEa402B237b92271A1EBe9A1011Eb42492228D61E

## 📝️ » Information
- Check every player for fake steamid or other something(100% protection)
- Have config file for change AppId
- Nosteam players are not displayed in server list to avoid ban

## 🔧 » Supported operating systems
| System  | Status |
|---------|--------|
| Windows |   ✅   |
| Linux   |   ✅   | 


## 🛠️ » Api and Hooks
#### IsPlayerNoSteam
Check player
```C#
IsSteam(ulong steamid)
IsSteam(Connection connection)
IsSteam(BasePlayer player)
```
##### Example 
```C#
bool IsPlayersSteam(BasePlayer player)
{
    if(Call<bool>("IsSteam", player) == true)
      return true;
    return false;
}
```
### Hooks
#### OnBeginPlayerSession
Returning a non-null value kick player with reason as value.
```C#
object OnBeginPlayerSession(Connection connection, bool isLicense)
{
  string status = isLicense ? "steam" : "nosteam";
  Puts($"{connection.userid} is {status} player c:");
  return null;
}
```
## 🧶 » Credits

[Harmony](https://github.com/pardeike/Harmony) patcher used in the project
