---
description: Elementos de interface do Windows Sockets 2 (Winsock) para MultiPoint e multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Elementos de interface do Windows Sockets 2 para MultiPoint e multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787597"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Elementos de interface do Windows Sockets 2 para MultiPoint e multicast

Os mecanismos que foram incorporados ao Windows Sockets 2 para utilização de recursos do MultiPoint podem ser resumidos da seguinte maneira:

-   Três bits de atributo na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatro sinalizadores definidos para o parâmetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Uma função, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para adicionar nós folha em uma sessão do MultiPoint.
-   Dois códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar o loopback do MultiPoint e o escopo de transmissões multicast.

As seções a seguir descrevem esses elementos de interface com mais detalhes:

-   [Semântica para unir as folhas do MultiPoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Como os protocolos MultiPoint existentes dão suporte a essas extensões](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
