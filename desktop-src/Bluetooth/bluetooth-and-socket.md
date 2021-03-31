---
title: Bluetooth e soquete
description: Cria um soquete para conexões de entrada ou saída.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth de Bluetooth
- soquete Bluetooth
- Bluetooth e soquete Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641187"
---
# <a name="bluetooth-and-socket"></a>Bluetooth e soquete

A função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) cria um soquete para conexões de entrada ou saída.:

Para criar um soquete usando Bluetooth, use as seguintes configurações:

-   O parâmetro *AF* da função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) é sempre definido como **AF \_ BTH** para soquetes Bluetooth.
-   O parâmetro de *tipo* da função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) é sempre **Sock \_ Stream**; **Sock \_** Os soquetes DGRAM não têm suporte do Bluetooth.
-   Para o parâmetro de *protocolo* , **BTHPROTO \_ RFCOMM** é o protocolo com suporte.

Para obter mais informações, consulte [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 