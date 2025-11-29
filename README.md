# 📘 KRAFTON TechLab Week03 – Unreal Engine Style 3D Editor & Rendering System
📌 프로젝트 개요

### 프로젝트명: Unreal Engine Style 3D Editor & Rendering System

#### 개발 기간: 1 week

#### 개발 환경: Visual Studio, DirectX 11, Windows 10/11

## 아키텍처: C++ 기반 Actor-Component 시스템
<img width="1911" height="1104" alt="image" src="https://github.com/user-attachments/assets/2aa029db-2fca-451d-aeaf-607d3256ccee" />


## 🚀 구현 완료 사항
### 🎨 1. Editor & Rendering System (눈에 보이는 세상)
#### 1.1 실시간 텍스트 렌더링 시스템(이호진)

파일: TextBillboard.hlsl, Week02/UI/

기능

ASCII 문자 → 텍스처 아틀라스 베이킹

UV 좌표 조작을 통한 임의 문자열 생성

Billboard 효과 (항상 카메라를 향함)

월드 공간의 UObject UUID 실시간 표시

기술

ViewInverse 행렬을 이용한 카메라 정렬

Alpha Testing 기반 텍스트 윤곽 처리

#### 1.2 Batch Line 렌더링 시스템

파일: ShaderLine.hlsl

기능

모든 Line을 하나의 Vertex/Index Buffer로 관리

D3D11_PRIMITIVE_TOPOLOGY_LINELIST 기반

World Grid, Bounding Box 시각화

성능 최적화

단일 Draw Call 처리

동적 버퍼 업데이트 지원


## 🖥 렌더링 파이프라인

World Grid (Show Flag)

Primitive Geometry (Lit/Unlit/Wireframe)

Bounding Boxes (Show Flag)

Billboard Text (UUID) (Show Flag)

Gizmo (선택된 객체)

셰이더 구성

Primitive.hlsl: 기본 메시

ShaderLine.hlsl: 라인/그리드

TextBillboard.hlsl: 빌보드 텍스트

##  성능 최적화

배치 렌더링: Draw Call 최소화

텍스처 아틀라스: 폰트 통합 관리

