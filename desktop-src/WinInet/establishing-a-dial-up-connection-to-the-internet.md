---
title: Estabelecendo uma conexão dial-up com a Internet
description: As funções a seguir são usadas para lidar com conexões de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008030"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="2aea4-103">Estabelecendo uma conexão dial-up com a Internet</span><span class="sxs-lookup"><span data-stu-id="2aea4-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="2aea4-104">As funções a seguir são usadas para lidar com conexões de modem.</span><span class="sxs-lookup"><span data-stu-id="2aea4-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="2aea4-105">**InternetAutodial**</span><span class="sxs-lookup"><span data-stu-id="2aea4-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="2aea4-106">**InternetAutodialHangup**</span><span class="sxs-lookup"><span data-stu-id="2aea4-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="2aea4-107">**InternetDial**</span><span class="sxs-lookup"><span data-stu-id="2aea4-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="2aea4-108">**InternetGetConnectedState**</span><span class="sxs-lookup"><span data-stu-id="2aea4-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="2aea4-109">**InternetGetConnectedStateEx**</span><span class="sxs-lookup"><span data-stu-id="2aea4-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="2aea4-110">**InternetHangUp**</span><span class="sxs-lookup"><span data-stu-id="2aea4-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="2aea4-111">**InternetGoOnline**</span><span class="sxs-lookup"><span data-stu-id="2aea4-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="2aea4-112">As funções de discagem do WinINet não dão suporte a conexões de discagem dupla, autenticação de cartão inteligente ou conexões que exigem certificação baseada no registro.</span><span class="sxs-lookup"><span data-stu-id="2aea4-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="2aea4-113">A partir do Windows Vista e do Windows Server 2008, as funções de dial-up do WinINet usam as [funções de Ras](/windows/desktop/RRAS/remote-access-service-functions) para estabelecer uma conexão discada.</span><span class="sxs-lookup"><span data-stu-id="2aea4-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="2aea4-114">O WinINet oferece suporte à funcionalidade documentada na função [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .</span><span class="sxs-lookup"><span data-stu-id="2aea4-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="2aea4-115">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="2aea4-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="2aea4-116">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="2aea4-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2aea4-117">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2aea4-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 