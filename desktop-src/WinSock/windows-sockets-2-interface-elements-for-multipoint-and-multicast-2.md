---
description: Windows Elementos de interface sockets 2 (Winsock) para multipoint e multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Elementos de interface Sockets 2 para Multipoint e Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf2422d8171a041f75ba8abed6ea490982187af3affb3d3c3d1349984210ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558848"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Elementos de interface Sockets 2 para Multipoint e Multicast

Os mecanismos que foram incorporados no Windows Sockets 2 para utilizar recursos de vários pontos podem ser resumidos da seguinte forma:

-   Três bits de atributo na [**estrutura \_ INFO WSAPROTOCOL.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Quatro sinalizadores definidos para *o parâmetro dwFlags* [**de WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Uma função, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)para adicionar nós folha a uma sessão de vários pontos.
-   Dois [**códigos de comando WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar o loopback de vários pontos e o escopo de transmissões multicast.

As seções a seguir descrevem esses elementos de interface mais detalhadamente:

-   [Semântica para junção de folhas de vários pontos](semantics-for-joining-multipoint-leaves-2.md)
-   [Como os protocolos multipoint existentes são suportados por essas extensões](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
