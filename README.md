# 프로젝트 개요
이 프로젝트는 SITL(Software In The Loop) 시뮬레이션 환경에서 가상 드론을 제어하고, OneDrone과 Mobius 플랫폼을 활용해 데이터를 송수신하는 통합 시스템을 구축하는 것을 목표로 합니다. 이 과정은 향후 경로 탐색 서버와의 통합을 목표로 하며, 드론의 최적 경로 탐색 및 관리를 지원하는 시스템을 구축하기 위함입니다.

# 현재 구현 내용
1. **SITL - OneDrone - Mobius 통신 연동**
    - SITL에서 가상 드론의 데이터를 **UDP** 프로토콜을 통해 **OneDrone**으로 전송합니다.
    - OneDrone에서는 수신한 데이터를 **MQTT** 프로토콜을 통해 **Mobius** 서버로 전달합니다.
    - 이를 통해 SITL에서 드론의 상태 정보를 Mobius 플랫폼에서 확인할 수 있도록 설정했습니다.

# 주요 구현 사항
- **드론 데이터 수집 및 전달**: SITL에서 드론의 위치, 배터리 상태, 기타 정보를 수집하여 OneDrone을 통해 Mobius에 전송하는 과정까지의 통신 흐름을 구현했습니다.
- **OneDrone과 Mobius 간 MQTT 통신**: Mobius 서버로 데이터가 정상적으로 수신되어, 드론 상태를 확인하고 모니터링할 수 있도록 구성했습니다.

# 경로 탐색 서버 구축을 위한 기반
- **경로 탐색 서버와의 통합 준비**: 현재 구현된 SITL - OneDrone - Mobius 통신은 향후 경로 탐색 서버와의 통합을 위해 구축된 것입니다. 경로 탐색 서버는 각 드론의 최적 경로를 계산하고, 이를 기반으로 드론을 실시간으로 제어할 수 있는 기능을 제공할 예정입니다.

