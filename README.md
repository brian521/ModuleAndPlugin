# ModuleAndPlugin

모듈 구조

Source/
├── MySpartaLog/                    # 모듈 메인 폴더
│   ├── Actor/                      # 액터 클래스들이 담길 폴더
│   │   ├── MyActor.cpp              
│   │   └── MyActor.h               
│   ├── MySpartaLog.Build.cs        # 모듈 빌드 설정 파일
│   ├── MySpartaLog.cpp             # 모듈 구현 파일 (Startup/Shutdown)
│   └── MySpartaLog.h               # 모듈 헤더 파일
├── ModuleAndPlugin.Target.cs           # 프로젝트 빌드 타겟 설정
└── ModuleAndPluginEditor.Target.cs     # 에디터 빌드 타겟 설정

--- 

플러그인 구조

Plugins/
└── MyNBCLog/                           # 플러그인 루트 폴더
    ├── MyNBCLog.uplugin                # 플러그인 메타데이터 (JSON)
    ├── Binaries/                       # 컴파일된 결과물 (자동 생성)
    ├── Content/                        # 블루프린트, 텍스처 등 에셋 폴더
    ├── Intermediate/                   # 빌드 시 발생하는 임시 파일 (자동 생성)
    ├── Resources/                      # 플러그인 아이콘 (Icon128.png 등)
    └── Source/                         # 소스 코드 루트
        └── MyNBCLog/                   # 모듈 폴더 (플러그인 이름과 동일하게 구성)
            ├── MyNBCLog.Build.cs       # 모듈 의존성 설정 파일
            ├── Private/                # 구현 파일 폴더 (내부 로직)
            │   └── TestActor.cpp
            └── Public/                 # 헤더 파일 폴더 (외부 노출)
                └── TestActor.h
