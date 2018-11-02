# 메쉬코리아 Java 개발자 개발환경 준비 가이드

## Tools

## Accounts

## Tips

### Maven Central Proxy

패키지 다운로드를 내부 리포지토리를 이용하면 더 빠르게 받을 수 있다.

 - Repository URL: `https://nexus.mm.meshkorea.net/repository/maven-central`
 - 인증필요
 -- ** LDAP (Jira/Confluence 계정) 연동이 현재 깨짐
 -- 임시 계정 `meshdev`/`20130118`
 
Project 별로 gradle 설정을 추가 하거나 globally 설정 할 수 있다. `~/.gradle/init.gradle` 편집:
 ```
 allprojects {
    repositories {
        mavenLocal()
        maven {
            url "https://nexus.mm.meshkorea.net/repository/maven-central"
            credentials {
                username = 'meshdev'
                password = '20130118'
            }
        }
    }
}
```
