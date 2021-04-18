---
description: O \_ tipo de enumeração de modos de medição de foco WPD \_ \_ descreve como um dispositivo deve decidir que parte de um quadro usar para definir o foco.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumeração de WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756516"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="52e68-103">\_Enumeração de \_ modos de medição de foco WPD \_</span><span class="sxs-lookup"><span data-stu-id="52e68-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="52e68-104">O tipo de enumeração de **\_ modos de \_ medição \_ de foco WPD** descreve como um dispositivo deve decidir que parte de um quadro usar para definir o foco.</span><span class="sxs-lookup"><span data-stu-id="52e68-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52e68-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="52e68-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="52e68-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52e68-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_modo de medição de foco WPD \_ \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="52e68-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="52e68-108">Indica que nenhum modo de foco foi especificado.</span><span class="sxs-lookup"><span data-stu-id="52e68-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="52e68-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ ponto central do modo de medição de \_ foco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="52e68-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="52e68-110">Concentra-se no centro da área emoldurada.</span><span class="sxs-lookup"><span data-stu-id="52e68-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="52e68-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_ \_ \_ \_ vários pontos do modo de medição de foco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="52e68-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="52e68-112">Determine o foco analisando várias partes da área de quadros.</span><span class="sxs-lookup"><span data-stu-id="52e68-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52e68-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52e68-113">Remarks</span></span>

<span data-ttu-id="52e68-114">Essa enumeração é especificada pela propriedade [de \_ \_ modo de \_ \_ medição \_ de foco de imagem WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="52e68-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e68-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52e68-115">Requirements</span></span>



| <span data-ttu-id="52e68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52e68-116">Requirement</span></span> | <span data-ttu-id="52e68-117">Valor</span><span class="sxs-lookup"><span data-stu-id="52e68-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e68-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52e68-118">Header</span></span><br/> | <dl> <span data-ttu-id="52e68-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="52e68-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e68-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="52e68-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e68-121">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="52e68-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




