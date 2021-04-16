---
title: ODJ_PROVISION_DATA
description: Definição de IDL de ODJ_PROVISION_DATA
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105772759"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="26055-103">Estrutura de ODJ_PROVISION_DATA</span><span class="sxs-lookup"><span data-stu-id="26055-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="26055-104">Especifica a estrutura de serialização mais externa usada pelas APIs de ingresso no domínio offline.</span><span class="sxs-lookup"><span data-stu-id="26055-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="26055-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26055-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="26055-106">Membros</span><span class="sxs-lookup"><span data-stu-id="26055-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="26055-107">ulVersion</span><span class="sxs-lookup"><span data-stu-id="26055-107">ulVersion</span></span>

<span data-ttu-id="26055-108">Isso deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="26055-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="26055-109">ulcBlobs</span><span class="sxs-lookup"><span data-stu-id="26055-109">ulcBlobs</span></span>

<span data-ttu-id="26055-110">Isso deve ser definido como o número de elementos na matriz pBlobs.</span><span class="sxs-lookup"><span data-stu-id="26055-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="26055-111">pBlobs</span><span class="sxs-lookup"><span data-stu-id="26055-111">pBlobs</span></span>

<span data-ttu-id="26055-112">Aponta para uma matriz de estruturas de ODJ_BLOB.</span><span class="sxs-lookup"><span data-stu-id="26055-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="26055-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="26055-113">See also</span></span>

[<span data-ttu-id="26055-114">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="26055-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="26055-115">**\_blob ODJ**</span><span class="sxs-lookup"><span data-stu-id="26055-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


