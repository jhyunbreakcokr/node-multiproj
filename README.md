multi-package project으로 구성해봤음.


# 장점
    1. 어쨌든 한 git-root 안에 monorepo으로 구성.

# 단점
    1. 의존성 liba을 매번 사용하는 측에서 `npm install`
       - 그것도 liba을 변경한다고 바로 복사 되는 것이 아니고,
       - `use-liba/node_modules`에 복사 되어서,
       - 해당 디렉토리를 전체 삭제하고 재시도하거나,
       - 그것도 아니면, liba의 버젼을 올려서 `npm install`이 설치해주도록 유도를 해야 할 것 같은데.
         - 자연스럽게 동작하지 못할 것 같다.
         
         
# 대안
    1. 정석적으로 private npm registry을 개설해 사용하거나,
    1. Yarn의 Workspaces 기능을 활용하거나
       - https://classic.yarnpkg.com/blog/2017/08/02/introducing-workspaces/
       - ..npm은 잘 지원할지 미지수.
