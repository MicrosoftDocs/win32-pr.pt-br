---
title: Estrutura de DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: A \_ estrutura ex de proteção de saída DRM \_ \_ contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende \_ a proteção de saída DRM \_ adicionando um número de versão.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Formato de mídia do Windows de estrutura de DRM_OUTPUT_PROTECTION_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797636"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="cdbb4-106">\_ \_ Estrutura ex de proteção de saída DRM \_</span><span class="sxs-lookup"><span data-stu-id="cdbb4-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="cdbb4-107">A **estrutura \_ \_ \_ ex de proteção de saída DRM** contém informações sobre uma tecnologia de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="cdbb4-108">Essa estrutura estende **a \_ \_ proteção de saída DRM** adicionando um número de versão.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdbb4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdbb4-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="cdbb4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="cdbb4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cdbb4-111">**DW**</span><span class="sxs-lookup"><span data-stu-id="cdbb4-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="cdbb4-112">Número da versão.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="cdbb4-113">**guidId**</span><span class="sxs-lookup"><span data-stu-id="cdbb4-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="cdbb4-114">GUID que identifica a tecnologia de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="cdbb4-115">**dwConfigData**</span><span class="sxs-lookup"><span data-stu-id="cdbb4-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="cdbb4-116">Dados de configuração para a tecnologia.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdbb4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdbb4-117">Remarks</span></span>

<span data-ttu-id="cdbb4-118">**DRM \_ Proteção de saída de áudio \_ \_ \_ ex** e **proteção de saída de vídeo DRM, por \_ \_ \_ \_ exemplo** , são definidas como **\_ \_ proteção de saída DRM** em instruções **typedef** .</span><span class="sxs-lookup"><span data-stu-id="cdbb4-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbb4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdbb4-119">Requirements</span></span>



| <span data-ttu-id="cdbb4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdbb4-120">Requirement</span></span> | <span data-ttu-id="cdbb4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cdbb4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbb4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdbb4-122">Header</span></span><br/> | <dl> <span data-ttu-id="cdbb4-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbb4-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdbb4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdbb4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbb4-125">**\_proteção de saída DRM \_**</span><span class="sxs-lookup"><span data-stu-id="cdbb4-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="cdbb4-126">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="cdbb4-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





