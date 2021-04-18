---
title: Estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: A \_ estrutura de restrições de vídeo analógica do WMDRM \_ \_ contém informações sobre uma restrição para reproduzir conteúdo como vídeo analógico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796136"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="0be4b-105">\_Estrutura de \_ restrições de vídeo analógico WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="0be4b-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="0be4b-106">A estrutura de **\_ \_ \_ restrições de vídeo analógica do WMDRM** contém informações sobre uma restrição para reproduzir conteúdo como vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="0be4b-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be4b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be4b-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="0be4b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0be4b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0be4b-109">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="0be4b-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="0be4b-110">Identificador de restrição.</span><span class="sxs-lookup"><span data-stu-id="0be4b-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0be4b-111">**dwRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="0be4b-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="0be4b-112">Dados de restrição.</span><span class="sxs-lookup"><span data-stu-id="0be4b-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0be4b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0be4b-113">Remarks</span></span>

<span data-ttu-id="0be4b-114">Essa estrutura é recebida quando você chama [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span><span class="sxs-lookup"><span data-stu-id="0be4b-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0be4b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be4b-115">Requirements</span></span>



| <span data-ttu-id="0be4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be4b-116">Requirement</span></span> | <span data-ttu-id="0be4b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0be4b-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0be4b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be4b-118">Header</span></span><br/> | <dl> <span data-ttu-id="0be4b-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be4b-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be4b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be4b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be4b-121">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="0be4b-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="0be4b-122">**\_restrições de \_ vídeo analógico WMDRM \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="0be4b-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





