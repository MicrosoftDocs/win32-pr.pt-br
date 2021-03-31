---
title: Compartilhamento de Conexão com a Internet
description: O BITS pode forçar uma conexão discada para redes domésticas que usam o compartilhamento de conexão com a Internet da Microsoft se o compartilhamento de conexão estiver configurado para discar quando os computadores na rede acessarem a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635015"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="c3e37-103">Compartilhamento de Conexão com a Internet</span><span class="sxs-lookup"><span data-stu-id="c3e37-103">Internet Connection Sharing</span></span>

<span data-ttu-id="c3e37-104">O BITS pode forçar uma conexão discada para redes domésticas que usam o compartilhamento de conexão com a Internet da Microsoft se o compartilhamento de conexão estiver configurado para discar quando os computadores na rede acessarem a Internet.</span><span class="sxs-lookup"><span data-stu-id="c3e37-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="c3e37-105">Para evitar uma conexão dial-up forçada, desabilite a opção **estabelecer uma conexão discada sempre que um computador em minha rede tentar acessar a Internet** no computador host de compartilhamento de conexão que compartilha sua conexão com a Internet.</span><span class="sxs-lookup"><span data-stu-id="c3e37-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="c3e37-106">Os computadores conectados ao computador host de compartilhamento de conexão pressupõem que eles têm uma conexão de rede, portanto, o BITS tentará transferir arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3e37-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="c3e37-107">Se a opção dial-up estiver desabilitada no computador host e o computador host não tiver uma conexão ativa, as transferências falharão com um erro transitório.</span><span class="sxs-lookup"><span data-stu-id="c3e37-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="c3e37-108">O BITS tentará novamente as transferências periodicamente.</span><span class="sxs-lookup"><span data-stu-id="c3e37-108">BITS will retry the transfers periodically.</span></span>

 

 




