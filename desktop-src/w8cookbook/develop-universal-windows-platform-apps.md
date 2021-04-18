---
title: Desenvolver aplicativos Plataforma Universal do Windows (UWP)
description: Desenvolver aplicativos Plataforma Universal do Windows (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105788663"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="9b97c-103">Desenvolver aplicativos Plataforma Universal do Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="9b97c-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="9b97c-104">Incentivamos todos os ISVs de aplicativos de desktop (Win32) a trazer seus aplicativos de desktop para o [plataforma universal do Windows (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) por meio da ponte de desktop.</span><span class="sxs-lookup"><span data-stu-id="9b97c-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="9b97c-105">Os aplicativos UWP também têm suporte na [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), portanto, é mais fácil para você atualizar os usuários para uma versão consistente automaticamente, reduzindo os custos de suporte.</span><span class="sxs-lookup"><span data-stu-id="9b97c-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="9b97c-106">Se seus aplicativos de área de trabalho não puderem ser convertidos usando a ponte de desktop, é altamente recomendável que você use um instalador que siga as práticas recomendadas e verifique se isso está totalmente testado.</span><span class="sxs-lookup"><span data-stu-id="9b97c-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="9b97c-107">Um instalador é a primeira experiência do usuário ou do seu cliente com seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b97c-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="9b97c-108">Geralmente, isso não funciona bem ou não foi totalmente testado para todos os cenários.</span><span class="sxs-lookup"><span data-stu-id="9b97c-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="9b97c-109">O [Kit de certificação de aplicativos para Windows](https://dev.windows.com/develop/app-certification-kit) pode ajudá-lo a testar a instalação e a desinstalação do seu aplicativo Win32 e a identificar o uso de APIs não documentadas, bem como outros problemas básicos de práticas recomendadas relacionadas ao desempenho antes de seus usuários.</span><span class="sxs-lookup"><span data-stu-id="9b97c-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="9b97c-110">Melhores práticas:</span><span class="sxs-lookup"><span data-stu-id="9b97c-110">Best practices:</span></span>

-   <span data-ttu-id="9b97c-111">Use instaladores que funcionam para versões de 32 bits e 64 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b97c-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="9b97c-112">Projete seus instaladores para execução em vários cenários (nível de usuário ou máquina).</span><span class="sxs-lookup"><span data-stu-id="9b97c-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="9b97c-113">Mantenha todos os recursos redistribuíveis do Windows no pacote original – se forem remontados, é possível que isso cause a perda do instalador.</span><span class="sxs-lookup"><span data-stu-id="9b97c-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="9b97c-114">Agende o tempo de desenvolvimento para seus instaladores. Eles geralmente são ignorados como um produto durante o ciclo de vida de desenvolvimento de software.</span><span class="sxs-lookup"><span data-stu-id="9b97c-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




