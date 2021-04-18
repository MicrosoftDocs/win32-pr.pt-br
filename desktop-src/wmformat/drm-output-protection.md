---
title: Estrutura de DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: A estrutura de proteção de saída do DRM \_ \_ contém informações sobre uma tecnologia de proteção de saída.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Formato de mídia do Windows de estrutura de DRM_OUTPUT_PROTECTION
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810814"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="bf2a3-105">Estrutura de proteção de \_ saída DRM \_</span><span class="sxs-lookup"><span data-stu-id="bf2a3-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="bf2a3-106">A estrutura de **\_ \_ proteção de saída do DRM** contém informações sobre uma tecnologia de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="bf2a3-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2a3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf2a3-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="bf2a3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bf2a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf2a3-109">**guidId**</span><span class="sxs-lookup"><span data-stu-id="bf2a3-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="bf2a3-110">GUID que identifica a tecnologia de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="bf2a3-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="bf2a3-111">**bConfigData**</span><span class="sxs-lookup"><span data-stu-id="bf2a3-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="bf2a3-112">Dados de configuração para a tecnologia.</span><span class="sxs-lookup"><span data-stu-id="bf2a3-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf2a3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf2a3-113">Remarks</span></span>

<span data-ttu-id="bf2a3-114">**DRM \_ A proteção de \_ saída de \_ áudio** e a **proteção de \_ \_ saída \_ de vídeo DRM** são definidas como **\_ \_ proteção de saída DRM** em instruções **typedef** .</span><span class="sxs-lookup"><span data-stu-id="bf2a3-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2a3-115">Requirements</span></span>



| <span data-ttu-id="bf2a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2a3-116">Requirement</span></span> | <span data-ttu-id="bf2a3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2a3-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2a3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf2a3-118">Header</span></span><br/> | <dl> <span data-ttu-id="bf2a3-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2a3-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2a3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf2a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2a3-121">**\_proteção de saída DRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="bf2a3-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="bf2a3-122">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="bf2a3-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





