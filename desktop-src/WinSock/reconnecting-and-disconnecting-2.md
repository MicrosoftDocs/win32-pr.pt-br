---
description: O destino padrão pode ser alterado simplesmente chamando WSPConnect novamente, mesmo que o soquete já esteja conectado. Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Reconectando e desconectando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827851"
---
# <a name="reconnecting-and-disconnecting"></a><span data-ttu-id="13b6e-104">Reconectando e desconectando</span><span class="sxs-lookup"><span data-stu-id="13b6e-104">Reconnecting and Disconnecting</span></span>

<span data-ttu-id="13b6e-105">O destino padrão pode ser alterado simplesmente chamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) novamente, mesmo que o soquete já esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="13b6e-105">The default destination may be changed by simply calling [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) again, even if the socket is already connected.</span></span> <span data-ttu-id="13b6e-106">Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um **WSPConnect** anterior.</span><span class="sxs-lookup"><span data-stu-id="13b6e-106">Any datagrams queued for receipt are discarded if the new address is different from the address specified in a previous **WSPConnect**.</span></span>

<span data-ttu-id="13b6e-107">Se o endereço fornecido para o soquete for todos os zeros, o Soquete será desconectado – o endereço remoto padrão será indeterminado, portanto chamadas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) retornarão o código de erro WSAENOTCONN, embora [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) ainda possam ser usados.</span><span class="sxs-lookup"><span data-stu-id="13b6e-107">If the address supplied for the socket is all zeros, the socket will be disconnected — the default remote address will be indeterminate, so [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) calls will return the error code WSAENOTCONN, although [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) may still be used.</span></span>

 

 
