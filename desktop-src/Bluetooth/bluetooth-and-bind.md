---
title: Bluetooth e associar
description: Bluetooth usa a função bind para associar a um soquete.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth e associar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7e7571e8d8a2c1a6dee29dc5f4839af5f1064bc5351cd3a13937f5750dd04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588486"
---
# <a name="bluetooth-and-bind"></a>Bluetooth e associar

Bluetooth usa a função [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) para associar a um soquete. para associar um soquete de Bluetooth, chame a função **bind** usando a estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) . Use a estrutura **SOCKADDR \_ BTH** com as seguintes configurações:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Em aplicativos cliente, o membro da porta deve ser zero para permitir que um ponto de extremidade local apropriado seja atribuído. Em aplicativos de servidor, o membro de porta deve ser um número de porta ou uma porta BT válida \_ \_ ; portas atribuídas automaticamente usando \_ a porta BT \_ podem ser consultadas subsequentemente com uma chamada para a função [**getsockname**](bluetooth-and-getsockname.md) . O intervalo válido para solicitar uma porta RFCOMM específica é de 1 a 30. os canais de servidor são recursos globais e apenas 30 canais de servidor estão disponíveis para RFCOMM em qualquer dispositivo Bluetooth, que deve ser compartilhado por todos os soquetes de Windows que pertencem à família de endereços Bluetooth. Se nenhum canal de servidor estiver disponível ou se o canal de servidor especificado já estiver reservado, a chamada de [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.

Após o retorno bem-sucedido da associação, o canal do servidor será reservado até que o soquete seja fechado. Use a função [**getsockname**](bluetooth-and-getsockname.md) para recuperar o número de canal para o registro de SDP.

Os aplicativos devem usar a alocação automática para o canal do servidor.

a função [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) não anuncia automaticamente o aplicativo de servidor usando o Bluetooth SDP; os aplicativos devem chamar a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para serem encontrados por aplicativos Bluetooth remotos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**associa**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 