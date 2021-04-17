---
title: Estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: A \_ estrutura ex de restrições de vídeo analógica do WMDRM \_ \_ \_ contém informações estendidas sobre uma restrição para reproduzir conteúdo como vídeo analógico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813571"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="86b64-105">\_ \_ \_ Estrutura ex de restrições de vídeo analógico WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="86b64-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="86b64-106">A **estrutura \_ \_ ex de \_ restrições \_ de vídeo analógica do WMDRM** contém informações estendidas sobre uma restrição para reproduzir conteúdo como vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="86b64-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b64-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86b64-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="86b64-108">Membros</span><span class="sxs-lookup"><span data-stu-id="86b64-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="86b64-109">**DW**</span><span class="sxs-lookup"><span data-stu-id="86b64-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="86b64-110">Número da versão.</span><span class="sxs-lookup"><span data-stu-id="86b64-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="86b64-111">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="86b64-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="86b64-112">ID da restrição.</span><span class="sxs-lookup"><span data-stu-id="86b64-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="86b64-113">**cbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="86b64-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="86b64-114">Tamanho dos dados de restrição em bytes.</span><span class="sxs-lookup"><span data-stu-id="86b64-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="86b64-115">**pbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="86b64-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="86b64-116">Dados de restrição.</span><span class="sxs-lookup"><span data-stu-id="86b64-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86b64-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="86b64-117">Remarks</span></span>

<span data-ttu-id="86b64-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="86b64-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b64-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b64-119">Requirements</span></span>



| <span data-ttu-id="86b64-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b64-120">Requirement</span></span> | <span data-ttu-id="86b64-121">Valor</span><span class="sxs-lookup"><span data-stu-id="86b64-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86b64-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86b64-122">Header</span></span><br/> | <dl> <span data-ttu-id="86b64-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b64-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86b64-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="86b64-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b64-125">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="86b64-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="86b64-126">**\_restrições de \_ vídeo \_ analógico WMDRM**</span><span class="sxs-lookup"><span data-stu-id="86b64-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





