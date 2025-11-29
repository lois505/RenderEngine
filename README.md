#  KRAFTON TechLab Week03 – Unreal Engine Style 3D Editor & Rendering System
 프로젝트 개요

### 프로젝트명: Unreal Engine Style 3D Editor & Rendering System

#### 개발 기간: 1 week

#### 개발 환경: Visual Studio, DirectX 11, Windows 10/11

## 아키텍처: C++ 기반 Actor-Component 시스템
<img width="1911" height="1104" alt="image" src="https://github.com/user-attachments/assets/2aa029db-2fca-451d-aeaf-607d3256ccee" />


###  구현 완료 사항
#### 1. 실시간 텍스트 렌더링 시스템(이호진)

파일: TextBillboard.hlsl, Week02/UI/

기능

텍스처 아틀라스를 이용한 텍스트 렌더링

Billboard 텍스트를 통한 월드 공간의 UObject UUID 실시간 표시

기술

ViewInverse 행렬을 이용한 카메라 정렬

#### 2. Batch Line 렌더링 시스템

파일: ShaderLine.hlsl

기능

모든 Line을 하나의 Vertex/Index Buffer로 관리

D3D11_PRIMITIVE_TOPOLOGY_LINELIST 기반

성능 최적화

단일 Draw Call 처리

동적 버퍼 업데이트 지원

#### 3. 렌더링 파이프라인 구축

기능

3D 물체 렌더링

병합비용 감소를 위한 Proxy(DTO)를 사용한 렌더링 로직 관심사 분리

#### 4. 수학 라이브러리 구축

기능

행렬 연산을 위한 Matrix및 Vector 구현

#### 5. 마우스 드래그 구현

기능 

마우스 드래그 시 기즈모의 역할에 따른 기능 수행(Translate, Rotate, Scale)



