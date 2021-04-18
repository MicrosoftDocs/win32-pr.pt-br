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
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="f6f44-103">Elementos de interface do Windows Sockets 2 para MultiPoint e multicast</span><span class="sxs-lookup"><span data-stu-id="f6f44-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="f6f44-104">Os mecanismos que foram incorporados ao Windows Sockets 2 para utilização de recursos do MultiPoint podem ser resumidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f6f44-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="f6f44-105">Três bits de atributo na estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="f6f44-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="f6f44-106">Quatro sinalizadores definidos para o parâmetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="f6f44-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="f6f44-107">Uma função, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para adicionar nós folha em uma sessão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="f6f44-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="f6f44-108">Dois códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar o loopback do MultiPoint e o escopo de transmissões multicast.</span><span class="sxs-lookup"><span data-stu-id="f6f44-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="f6f44-109">As seções a seguir descrevem esses elementos de interface com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="f6f44-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="f6f44-110">Semântica para unir as folhas do MultiPoint</span><span class="sxs-lookup"><span data-stu-id="f6f44-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="f6f44-111">Como os protocolos MultiPoint existentes dão suporte a essas extensões</span><span class="sxs-lookup"><span data-stu-id="f6f44-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
