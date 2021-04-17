---
description: O \_ tipo de \_ enumeração valores de status corrigidos de cor WPD \_ \_ descreve o status de correção de cor de um arquivo de imagem ou de vídeo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumeração de WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791598"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="6ab72-103">\_Enumeração de \_ valores de status corrigidos de cor WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="6ab72-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="6ab72-104">O tipo de enumeração **\_ \_ \_ \_ valores de status corrigidos de cor WPD** descreve o status de correção de cor de um arquivo de imagem ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6ab72-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ab72-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="6ab72-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6ab72-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6ab72-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_status corrigido de cor WPD \_ \_ \_ não \_ corrigido**</span><span class="sxs-lookup"><span data-stu-id="6ab72-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6ab72-108">A imagem não foi corrigida por cor.</span><span class="sxs-lookup"><span data-stu-id="6ab72-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="6ab72-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_status corrigido de cor WPD \_ \_ \_ corrigido**</span><span class="sxs-lookup"><span data-stu-id="6ab72-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6ab72-110">A imagem foi corrigida por cor.</span><span class="sxs-lookup"><span data-stu-id="6ab72-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="6ab72-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**o \_ status corrigido da cor WPD \_ \_ \_ \_ não deve \_ ser \_ corrigido**</span><span class="sxs-lookup"><span data-stu-id="6ab72-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6ab72-112">A imagem não foi, e não deve ser, a cor corrigida.</span><span class="sxs-lookup"><span data-stu-id="6ab72-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ab72-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ab72-113">Remarks</span></span>

<span data-ttu-id="6ab72-114">Indica o status corrigido da cor de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="6ab72-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="6ab72-115">Essa enumeração é usada pela propriedade [ \_ \_ \_ \_ status corrigido de cor de imagem WPD](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6ab72-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab72-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ab72-116">Requirements</span></span>



| <span data-ttu-id="6ab72-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab72-117">Requirement</span></span> | <span data-ttu-id="6ab72-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ab72-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab72-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ab72-119">Header</span></span><br/> | <dl> <span data-ttu-id="6ab72-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab72-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab72-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ab72-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab72-122">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="6ab72-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




