---
description: O arquivo de cabeçalho Winternl. h expõe protótipos de APIs internas do Windows. Não há biblioteca de importação associada, portanto os desenvolvedores devem usar a vinculação dinâmica em tempo de execução para chamar as funções descritas neste arquivo de cabeçalho.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Chamando APIs internas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920311"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="ce921-104">Chamando APIs internas</span><span class="sxs-lookup"><span data-stu-id="ce921-104">Calling Internal APIs</span></span>

<span data-ttu-id="ce921-105">O arquivo de cabeçalho Winternl. h expõe protótipos de APIs internas do Windows.</span><span class="sxs-lookup"><span data-stu-id="ce921-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="ce921-106">Não há biblioteca de importação associada, portanto os desenvolvedores devem usar a vinculação dinâmica em tempo de execução para chamar as funções descritas neste arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ce921-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="ce921-107">As funções e estruturas em Winternl. h são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para a próxima e, possivelmente, entre os Service Packs de cada versão.</span><span class="sxs-lookup"><span data-stu-id="ce921-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="ce921-108">Para manter a compatibilidade do seu aplicativo, você deve usar as funções públicas equivalentes em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ce921-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="ce921-109">Mais informações estão disponíveis no arquivo de cabeçalho, Winternl. h, e a documentação para cada função.</span><span class="sxs-lookup"><span data-stu-id="ce921-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="ce921-110">Se você usar essas funções, poderá acessá-las por meio da vinculação dinâmica em tempo de execução usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="ce921-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="ce921-111">Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ce921-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="ce921-112">As alterações de assinatura, no entanto, podem não ser detectáveis.</span><span class="sxs-lookup"><span data-stu-id="ce921-112">Signature changes, however, may not be detectable.</span></span>

 

 
