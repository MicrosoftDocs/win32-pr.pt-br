---
title: Versões do sistema operacional
description: Esse tipo de dados DWORD deve conter o tipo de sistema operacional na palavra de ordem superior e o número de versão do sistema operacional na palavra de ordem inferior. Os valores possíveis para o sistema operacional são listados na tabela a seguir.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Armazenamento estruturado das versões do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754486"
---
# <a name="operating-system-versions"></a><span data-ttu-id="31300-105">Versões do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="31300-105">Operating System Versions</span></span>

<span data-ttu-id="31300-106">Esse tipo de dados **DWORD** deve conter o tipo de sistema operacional na palavra de ordem superior e o número de versão do sistema operacional na palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="31300-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="31300-107">Os valores possíveis para o sistema operacional são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="31300-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="31300-108">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="31300-108">Operating system</span></span>       | <span data-ttu-id="31300-109">Valor</span><span class="sxs-lookup"><span data-stu-id="31300-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="31300-110">Windows de 32 bits (Win32)</span><span class="sxs-lookup"><span data-stu-id="31300-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="31300-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="31300-111">0x0002</span></span> |
| <span data-ttu-id="31300-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="31300-112">Macintosh</span></span>              | <span data-ttu-id="31300-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="31300-113">0x0001</span></span> |
| <span data-ttu-id="31300-114">Windows de 16 bits (Win16)</span><span class="sxs-lookup"><span data-stu-id="31300-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="31300-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="31300-115">0x0000</span></span> |



 

<span data-ttu-id="31300-116">Para sistemas operacionais Microsoft Windows, a versão do sistema operacional é a palavra de ordem inferior retornada pela função [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) .</span><span class="sxs-lookup"><span data-stu-id="31300-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="31300-117">Para o Microsoft Windows, o código de exemplo a seguir define corretamente a versão do sistema operacional de origem.</span><span class="sxs-lookup"><span data-stu-id="31300-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 