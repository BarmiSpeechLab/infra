## 💡Infra 레포지토리입니다.

> 해당 레포지토리는 Nginx 환경과 RabbitMQ 환경을 정의합니다.
- Nginx: 리버스 프록시 및 SSL 종료 지점입니다. 
    - 80→443 리다이렉트
    - 프론트엔드(`/` → `frontend:3000`)
    - 백엔드 API(`/api/` → `backend:8080`)
    - OpenVidu WebSocket(`5443` → `openvidu-dev:5443`)
- RabbitMQ: 메시지 브로커 환경입니다.

## 🔗 기술 개발 문서
- [RabbitMQ란 무엇인가요?](https://www.notion.so/RabbitMQ-2f4fc74069a680e1b7fedc75387541c7?source=copy_link)
- [RabbitMQ 기술 설계](https://www.notion.so/RabbitMQ-2f4fc74069a68006a3e7d84af7388e2e?source=copy_link)
- [Nginx에 대하여](https://www.notion.so/Nginx-2f7fc74069a680048dcde22b080339f9?source=copy_link)
- [WebRTC Openvidu 배포 환경 이슈 해결](https://www.notion.so/WebRTC-Openvidu-2fefc74069a68060a121e2f73fcd3ef2?source=copy_link)

## 📁 디렉토리 구조

```
infra/
├── nginx/
│   ├── nginx.conf        # Nginx 기본 설정
│   └── conf.d/
│       └── default.conf  # 가상 호스트 및 라우팅 설정
└── rabbitmq/
    ├── rabbitmq.conf     # RabbitMQ 기본 설정
    └── definitions.json  # vhost/권한/익스체인지/큐 정의
```
