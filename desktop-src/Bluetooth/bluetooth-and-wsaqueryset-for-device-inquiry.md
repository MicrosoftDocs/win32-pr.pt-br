---
title: Bluetooth e WSAQUERYSET para a consulta do dispositivo
description: usado para facilitar a descoberta de dispositivos e serviços no namespace Bluetooth, NS \_ BTH.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth e WSAQUERYSET para Bluetooth de consulta do dispositivo
- WSAQUERYSET Bluetooth, para consulta do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a9250670fda52f2ecdc27ffee949b12049b8ec2860b7ee2df23631c4469076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959275"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth e WSAQUERYSET para a consulta do dispositivo

no Bluetooth, a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , é usada para facilitar a descoberta de dispositivos e serviços no namespace Bluetooth, NS \_ BTH.

As funções [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usam a estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obter informações sobre o processo de consulta do dispositivo. A tabela a seguir lista e descreve os valores de membro na estrutura **WSAQUERYSET** .

| Membro                      | Entrada para WSALookupServiceBegin com \_ contêineres Lup especificados                                                                                                                                              | Valor retornado de WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Deve ser definido como **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) retornado pelo sistema.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | Não usado.                                                                                                                                                                                                  | Pode ter um ou mais destes sinalizadores definidos: **BTHNS \_ resultado \_ dispositivo \_ conectado** especifica que o dispositivo está conectado.<br/> **BTHNS \_ RESULTADO o \_ dispositivo \_ lembrado** especifica que o dispositivo é um dispositivo lembrado. Nem todos os dispositivos lembrados são autenticados.<br/> **BTHNS \_ O \_ dispositivo de resultado \_ autenticado** especifica que o dispositivo é autenticado, emparelhado ou acoplado. Todos os dispositivos autenticados são lembrados.<br/> |
| **lpszServiceInstanceName** | Não usado.                                                                                                                                                                                                  | nome de exibição do dispositivo, retornado originalmente de uma operação de solicitação de nome Bluetooth remoto e possivelmente atualizado pelo usuário local. Retornado se **o \_ \_ nome de retorno de Lup** for especificado.                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | Não usado.                                                                                                                                                                                                  | o campo de dispositivo (COD) de Bluetooth de 32 bits mapeado para o membro **dados1** do GUID. Retornado se **o \_ \_ tipo de retorno Lup** for especificado.                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Deve ser NS \_ BTH.                                                                                                                                                                                           | Retorna **ns \_ BTH**.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | Não usado.                                                                                                                                                                                                  | Não usado.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | Não usado.                                                                                                                                                                                                  | Indica o número de elementos na matriz de estruturas [**de \_ informações de CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) .                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | Não usado.                                                                                                                                                                                                  | Ponteiro para uma estrutura de [**\_ informações de CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) com seu membro **localaddr. lpSockAddr** apontando para uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com o endereço do dispositivo remoto. Retornado se **o \_ \_ endereço de retorno de Lup** for especificado.                                                                                                                                                                  |
| **lpBlob**                  | Opcional. Pode apontar para uma estrutura de [**blob**](/windows/desktop/api/nspapi/ns-nspapi-blob) que aponta para uma estrutura de [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) que pode limitar o comprimento de operações de consulta de dispositivo não armazenadas em cache. | Ponteiro para uma estrutura de [**blob**](/windows/desktop/api/nspapi/ns-nspapi-blob) que aponta para uma estrutura de [**\_ \_ informações do dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) . **lpBlob** será retornado se **Lup \_ retornar \_ blob** for especificado. Especifique **o \_ \_ nome de retorno do Lup** para recuperar o campo de nome das **\_ \_ informações do dispositivo BTH**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSAQUERYSET para o serviço de conjunto](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET para consulta de serviço](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_informações do dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**\_dispositivo de consulta BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**informações de CSADDR \_**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

