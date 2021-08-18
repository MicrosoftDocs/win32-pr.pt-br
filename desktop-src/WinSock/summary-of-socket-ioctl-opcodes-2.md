---
description: alguns dos opcodes de soquete do IOCTL para Windows sockets 2 são resumidos na tabela a seguir.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Resumo dos opcodes do slot IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559656"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Resumo dos opcodes do slot IOCTL

alguns dos opcodes de soquete do IOCTL para Windows sockets 2 são resumidos na tabela a seguir. Informações mais detalhadas estão na referência do Winsock em [**IOCTLs do Winsock**](winsock-ioctls.md) e na função [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) . Há outros novos opcodes do IOCTL específicos de protocolo que podem ser encontrados no anexo específico do protocolo.

Uma lista completa de [**IOCTLs do Winsock**](winsock-ioctls.md) está disponível na referência do Winsock.



| Opcode                                                      | Tipo de entrada                               | Tipo de saída                                 | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Longo não assinado                            | <Not used>                            | Habilita ou desabilita o modo de não bloqueio no soquete.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Longo não assinado                               | Determina a quantidade de dados que podem ser lidos atomicamente do soquete.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Determina se todos os dados OOB foram ou não lidos.                                                                                                                                                              |
| SIO \_ associar \_ identificador                                      | Dependente da API complementar                  | <Not used>                            | Associa o soquete ao identificador especificado de uma interface complementar.                                                                                                                                          |
| SIO \_ habilitar \_ \_ enfileiramento circular                             | <Not used>                         | <Not used>                            | Habilita o enfileiramento circular.                                                                                                                                                                                          |
| SIO \_ localizar \_ rota                                            | estrutura [**SOCKADDR**](sockaddr-2.md) | <Not used>                            | Solicita que a rota para o endereço especificado seja descoberta.                                                                                                                                                      |
| SIO \_ liberar                                                  | <Not used>                         | <Not used>                            | Descarta o conteúdo atual da fila de envio.                                                                                                                                                                    |
| SIO \_ obter \_ endereço de difusão \_                                | <Not used>                         | estrutura [**SOCKADDR**](sockaddr-2.md)    | Recupera o endereço de difusão específico do protocolo a ser usado em [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)).                                                                                                                  |
| SIO \_ obter \_ QoS                                               | <Not used>                         | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Recupera as especificações de fluxo atuais para o soquete.                                                                                                                                                              |
| SIO \_ obter \_ QoS de grupo \_                                        | <Not used>                         | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Reservado.                                                                                                                                                                                                          |
| \_loopback do MultiPoint sio \_                                   | BOOL                                     | <Not used>                            | Controla se os dados enviados em uma sessão do MultiPoint também serão recebidos pelo mesmo soquete no host local.                                                                                                     |
| \_escopo de multicast sio \_                                       | INT                                      | <Not used>                            | Especifica o escopo sobre o qual ocorrerá as transmissões multicast.                                                                                                                                                 |
| SIO \_ definir \_ QoS                                               | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Estabelece novas especificações de fluxo para o soquete.                                                                                                                                                                |
| QoS do grupo de SIO \_ set \_ \_                                        | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Reservado.                                                                                                                                                                                                          |
| \_identificador de conversão sio \_                                      | INT                                      | Companion-dependente da API                     | Obtém um identificador correspondente para o soquete *s* que é válido no contexto de uma interface complementar.                                                                                                               |
| \_consulta da \_ interface de roteamento do sio \_                              | [**SOCKADDR**](sockaddr-2.md)           | [**SOCKADDR**](sockaddr-2.md)              | Obtém o endereço da interface local que deve ser usado para enviar para o endereço especificado.                                                                                                                   |
| \_alteração da \_ interface de roteamento sio \_                             | [**SOCKADDR**](sockaddr-2.md)           | <Not used>                            | Solicita notificação de alterações nas informações relatadas por meio da \_ consulta da interface de roteamento do sio \_ \_ para o endereço especificado.                                                                                         |
| [**\_consulta de \_ lista de endereços do sio \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**Endereço do soquete \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode ser associado. A lista de endereços varia de acordo com a família de endereços e alguns endereços são excluídos da lista. |
| \_alteração da \_ lista de endereços do sio \_                                  | <Not used>                         | <Not used>                            | Solicita notificação de alterações nas informações relatadas por meio da consulta da lista de endereços do SIO \_ \_ \_                                                                                                                         |
| \_identificador de \_ \_ destino PNP de consulta \_ sio                             | <Not used>                         | SSA                                      | Obtém o descritor de soquete do próximo provedor na cadeia em que o soquete atual depende em relação ao PnP.                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
