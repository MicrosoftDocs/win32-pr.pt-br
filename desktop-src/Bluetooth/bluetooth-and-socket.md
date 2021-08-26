---
title: Bluetooth soquete
description: Cria um soquete para conexões de entrada ou saída.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- soquete Bluetooth
- Bluetooth e soquete Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004296"
---
# <a name="bluetooth-and-socket"></a>Bluetooth soquete

A [**função de**](/windows/desktop/api/winsock2/nf-winsock2-socket) soquete cria um soquete para conexões de entrada ou saída.:

Para criar um soquete usando Bluetooth, use as seguintes configurações:

-   O *parâmetro af* da função de [**soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) é sempre definido como AF **\_ BTH** para Bluetooth soquetes.
-   O *parâmetro de* tipo da função de [**soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) é **sempre SOCK \_ STREAM**; **SOCK \_ Não há** suporte para soquetes DGRAM Bluetooth.
-   Para o *parâmetro de* protocolo, o **PROTOCOLO \_ RFCOMM BTHPROTO** é o protocolo com suporte.

Para obter mais informações, [consulte Windows Soquetes](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 