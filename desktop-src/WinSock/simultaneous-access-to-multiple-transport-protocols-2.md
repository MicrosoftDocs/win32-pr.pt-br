---
description: Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com o Windows Sockets para ser acessível a um aplicativo.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acesso simultâneo a vários protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781460"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Acesso simultâneo a vários protocolos de transporte

Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com o Windows Sockets para ser acessível a um aplicativo. A \_ biblioteca de32.dll Ws2 exporta um conjunto de funções para facilitar o processo de registro. Isso inclui a criação de um novo registro e a remoção de um existente.

Quando novos registros são criados, o chamador (ou seja, o script de instalação do fornecedor da pilha) fornece uma ou mais estruturas [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) preenchidas contendo um conjunto completo de informações sobre o protocolo. Para obter mais informações, consulte [SPI do Windows Sockets 2](about-the-winsock-spi.md). Qualquer pilha de transporte instalada dessa maneira é conhecida como um provedor de serviços do Windows Sockets.

No Windows XP com Service Pack 2 (SP2), Windows Server 2003 com Service Pack 1 (SP1) e Windows Vista e posterior. o catálogo Winsock que contém uma lista de provedores de transporte e de namespace instalados pode ser exibido em um prompt de comando com o seguinte comando:

**netsh winsock mostrar catálogo**

O SDK (Software Development Kit) do Microsoft Windows inclui *Sporder.exe*, que permite ao usuário exibir e modificar a ordem em que os provedores de serviço são enumerados. Usando *Sporder.exe*, um usuário pode estabelecer manualmente uma pilha de protocolo TCP/IP específica como o provedor TCP/IP padrão se mais de uma dessas pilhas estiver presente.

O aplicativo *Sporder.exe* usa funções exportadas de *Sporder.dll* para reordenar os provedores de serviços. Como resultado, os aplicativos de instalação podem usar a interface fornecida pelo *Sporder.dll* para reordenar programaticamente os provedores de serviço.

-   [Protocolos em camadas e cadeias de protocolos](layered-protocols-and-protocol-chains-2.md)
-   [Usando vários protocolos](using-multiple-protocols-2.md)
-   [Restrições de vários provedores em Select](multiple-provider-restrictions-on-select-2.md)

 

 
