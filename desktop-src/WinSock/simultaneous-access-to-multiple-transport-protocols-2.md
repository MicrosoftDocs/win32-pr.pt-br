---
description: Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com Windows Soquetes para ser acessível a um aplicativo.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acesso simultâneo a vários protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9648a7ffe1c4c0b1627ea46cd2956b48ba574adb468d750a2c4095a32783746f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111543"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Acesso simultâneo a vários protocolos de transporte

Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com Windows Soquetes para ser acessível a um aplicativo. A biblioteca Ws2 \_32.dll exporta um conjunto de funções para facilitar o processo de registro. Isso inclui a criação de um novo registro e a remoção de um existente.

Quando novos registros são criados, o chamador (ou seja, o script de instalação do fornecedor da pilha) fornece uma ou mais estruturas [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que contêm um conjunto completo de informações sobre o protocolo. Para obter mais informações, [consulte Windows Sockets 2 SPI](about-the-winsock-spi.md). Qualquer pilha de transporte instalada dessa maneira é conhecida como um provedor de serviços Windows Sockets.

No Windows XP com Service Pack 2 (SP2), Windows Server 2003 com Service Pack 1 (SP1) e Windows Vista e posterior. O catálogo winsock que contém uma lista de provedores de transporte e namespace instalados pode ser exibido em um prompt de comando com o seguinte comando:

**netsh winsock show catalog**

O Microsoft Windows Software Development Kit (SDK) inclui *Sporder.exe*, que permite que o usuário veja e modifique a ordem na qual os provedores de serviços são enumerados. Usando *Sporder.exe*, um usuário poderá estabelecer manualmente uma pilha de protocolo TCP/IP específica como o provedor TCP/IP padrão se mais de uma dessas pilhas estiver presente.

O *Sporder.exe* aplicativo usa funções exportadas *de* Sporder.dllpara reordenar os provedores de serviços. Como resultado, os aplicativos de instalação podem usar a interface fornecida *peloSporder.dll* para reordenar programaticamente provedores de serviços.

-   [Protocolos em camadas e cadeias de protocolo](layered-protocols-and-protocol-chains-2.md)
-   [Usando vários protocolos](using-multiple-protocols-2.md)
-   [Várias restrições de provedor em Selecionar](multiple-provider-restrictions-on-select-2.md)

 

 
