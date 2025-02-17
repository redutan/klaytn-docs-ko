# 트랜잭션 에러 코드 <a id="transaction-error-codes"></a>

Klaytn은 트랜잭션 영수증의 `txError` 필드를 통해 트랜잭션 실행이 실패한 원인을 개발자분들께 알려드립니다. 이 필드는 트랜잭션 실행이 실패한 경우에만 존재합니다. 스토리지와 네트워크 대역폭을 절약하기 위해 `txError`는 정숫값으로 표현됩니다. 아래 표는 `txError` 코드와 의미를 설명합니다.

| 오류 코드 | 설명                                                |
|:----- |:------------------------------------------------- |
| 0x02  | 스마트 컨트랙트 실행 도중 VM 오류가 발생하였습니다.                    |
| 0x03  | 최대 호출 뎁스를 초과하였습니다.                                |
| 0x04  | 컨트랙트 주소가 충돌합니다.                                   |
| 0x05  | 컨트랙트 생성 코드의 스토리지의 가스가 부족합니다.                      |
| 0x06  | evm: 최대 코드 크기를 초과하였습니다.                           |
| 0x07  | 가스가 부족합니다.                                        |
| 0x08  | evm: 쓰기가 방지되어 있습니다.                               |
| 0x09  | evm: 실행이 번복되었습니다.                                 |
| 0x0a  | 트랜잭션의 Opcode 연산 비용의 한계가 \(100000000\)에 도달하였습니다. |
| 0x0b  | 계정이 이미 존재합니다.                                     |
| 0x0c  | 프로그램 계정\(예를 들어, 코드 및 스토리지를 갖고 있는 계정\)이 아닙니다.    |
| 0x0d  | Human-readable address가 지원되지 않습니다.                |
| 0x0e  | 트랜잭션 수수료의 비율이 \[1, 99\] 범위를 벗어났습니다.             |
| 0x0f  | AccountKeyFail을 업데이트할 수 없습니다.                     |
| 0x10  | 다른 계정 키 유형입니다.                                    |
| 0x11  | AccountKeyNil을 계정으로 초기화할 수 없습니다.                  |
| 0x12  | 공개키가 곡선상에 없습니다.                                   |
| 0x13  | 키의 weight가 0입니다.                                  |
| 0x14  | 키를 일련화할 수 없습니다.                                   |
| 0x15  | 중복된 키입니다.                                         |
| 0x16  | 가중 합 오버플로우가 발생하였습니다.                              |
| 0x17  | 만족시킬 수 없는 임계 값입니다. 키들의 가중 합이 임계 값보다 작습니다.         |
| 0x18  | 길이가 0입니다.                                         |
| 0x19  | 길이가 너무 깁니다.                                       |
| 0x1a  | nested composite 타입입니다.                           |
| 0x1b  | 기존 트랜잭션은 기존 계정 키를 사용해야 합니다.                       |
| 0x1c  | 더는 지원하지 않는 기능입니다.                                 |
| 0x1d  | 지원하지 않습니다.                                        |
| 0x1e  | 스마트 컨트랙트 코드 형식이 잘못되었습니다.                          |

