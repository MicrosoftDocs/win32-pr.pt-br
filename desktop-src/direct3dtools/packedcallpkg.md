---
description: Representa um pacote de quatro chamadas.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PackedCallPkg
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919857"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span data-ttu-id="90a89-103"><span id="vspixengine.packedcallpkg"></span>Estrutura PackedCallPkg</span><span class="sxs-lookup"><span data-stu-id="90a89-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg structure</span></span>

<span data-ttu-id="90a89-104">Representa um pacote de quatro chamadas.</span><span class="sxs-lookup"><span data-stu-id="90a89-104">Represents a package of four calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90a89-105">Syntax</span></span>


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a><span data-ttu-id="90a89-106">Membros</span><span class="sxs-lookup"><span data-stu-id="90a89-106">Members</span></span>

<span data-ttu-id="90a89-107">**pcp1**</span><span class="sxs-lookup"><span data-stu-id="90a89-107">**pcp1**</span></span>  
<span data-ttu-id="90a89-108">A primeira chamada no pacote.</span><span class="sxs-lookup"><span data-stu-id="90a89-108">The first call in the package.</span></span>

<span data-ttu-id="90a89-109">**pcp2**</span><span class="sxs-lookup"><span data-stu-id="90a89-109">**pcp2**</span></span>  
<span data-ttu-id="90a89-110">A segunda chamada no pacote.</span><span class="sxs-lookup"><span data-stu-id="90a89-110">The second call in the package.</span></span>

<span data-ttu-id="90a89-111">**pcp3**</span><span class="sxs-lookup"><span data-stu-id="90a89-111">**pcp3**</span></span>  
<span data-ttu-id="90a89-112">A terceira chamada no pacote.</span><span class="sxs-lookup"><span data-stu-id="90a89-112">The third call in the package.</span></span>

<span data-ttu-id="90a89-113">**pcp4**</span><span class="sxs-lookup"><span data-stu-id="90a89-113">**pcp4**</span></span>  
<span data-ttu-id="90a89-114">A quarta chamada no pacote.</span><span class="sxs-lookup"><span data-stu-id="90a89-114">The fourth call in the package.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a89-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a89-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="90a89-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90a89-116">Header</span></span></p></td><td><span data-ttu-id="90a89-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="90a89-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



