---
description: WSPGetSockName é usado para recuperar o endereço local para soquetes associados.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinando nomes locais e remotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010492"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="f7971-103">Determinando nomes locais e remotos</span><span class="sxs-lookup"><span data-stu-id="f7971-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="f7971-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) é usado para recuperar o endereço local para soquetes associados.</span><span class="sxs-lookup"><span data-stu-id="f7971-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="f7971-105">Isso é especialmente útil quando uma chamada [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) foi feita sem fazer um [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) primeiro; **WSPGetSockName** fornece o único meio para determinar a associação local que foi definida implicitamente pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="f7971-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="f7971-106">Depois que uma conexão tiver sido configurada, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) poderá ser usado para determinar o endereço do ponto ao qual um soquete está conectado.</span><span class="sxs-lookup"><span data-stu-id="f7971-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
