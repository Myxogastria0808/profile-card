# profile-card

自己紹介をHaskellで記述した。

```haskell
module Main (main) where
import Text.Pretty.Simple (pPrint)

data Profile = Profile {
    handleName :: String,
    department :: String,
    grade :: Int,
    gensiken :: Gensiken,
    hobbies :: [String]
  }
  deriving (Show)

data Gensiken = Gensiken {
    group :: String,
    position :: String,
    activityDetails :: String
  }
  deriving (Show)

main :: IO ()
main = do
  let profile = Profile { handleName = "Myxogastria0808",
            department = "情報科学類",
            grade = 4,
            gensiken = Gensiken { group = "美少女ゲーム班",
                  position = "スクリプター",
                  activityDetails = "ノベルゲームエンジン"
                },
            hobbies = [ "Nix", "Haskell", "圏論", "お絵描き" ]
          }
  pPrint profile

```
