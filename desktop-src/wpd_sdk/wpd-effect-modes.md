---
description: O \_ tipo de enumeração de modos de efeito WPD \_ descreve vários efeitos visuais que podem ser aplicados a uma imagem.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumeração de WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807247"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="0fa26-103">Enumeração de modos de \_ efeito WPD \_</span><span class="sxs-lookup"><span data-stu-id="0fa26-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="0fa26-104">O tipo de enumeração de **\_ \_ modos de efeito WPD** descreve vários efeitos visuais que podem ser aplicados a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="0fa26-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fa26-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="0fa26-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0fa26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0fa26-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_modo de efeito WPD \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="0fa26-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="0fa26-108">Nenhum efeito foi especificado.</span><span class="sxs-lookup"><span data-stu-id="0fa26-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="0fa26-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_cor do \_ modo de efeito WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0fa26-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0fa26-110">A imagem deve ser colorida.</span><span class="sxs-lookup"><span data-stu-id="0fa26-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="0fa26-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_ \_ modo de efeito \_ de WPD preto \_ e \_ branco**</span><span class="sxs-lookup"><span data-stu-id="0fa26-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="0fa26-112">A imagem deve ser preta e branca.</span><span class="sxs-lookup"><span data-stu-id="0fa26-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="0fa26-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**modo de efeito de WPD de \_ \_ \_ sépia**</span><span class="sxs-lookup"><span data-stu-id="0fa26-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="0fa26-114">A imagem deve ser sépia.</span><span class="sxs-lookup"><span data-stu-id="0fa26-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fa26-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fa26-115">Remarks</span></span>

<span data-ttu-id="0fa26-116">Essa enumeração é usada pela propriedade [ \_ modo de \_ \_ efeito de \_ imagem ainda em WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa26-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa26-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fa26-117">Requirements</span></span>



| <span data-ttu-id="0fa26-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fa26-118">Requirement</span></span> | <span data-ttu-id="0fa26-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0fa26-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa26-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fa26-120">Header</span></span><br/> | <dl> <span data-ttu-id="0fa26-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa26-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fa26-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fa26-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa26-123">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="0fa26-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




