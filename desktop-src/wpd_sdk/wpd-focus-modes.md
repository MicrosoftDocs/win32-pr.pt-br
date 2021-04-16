---
description: O \_ tipo de enumeração de modos de foco WPD \_ descreve o modo de foco usado por um dispositivo de captura de imagem ainda.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumeração de WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750400"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="cf2ef-103">Enumeração de modos de \_ foco WPD \_</span><span class="sxs-lookup"><span data-stu-id="cf2ef-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="cf2ef-104">O tipo de enumeração de **\_ \_ modos de foco WPD** descreve o modo de foco usado por um dispositivo de captura de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf2ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf2ef-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="cf2ef-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cf2ef-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf2ef-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**foco de WPD \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="cf2ef-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="cf2ef-108">O modo de foco não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="cf2ef-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_manual de foco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf2ef-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="cf2ef-110">Especifica o foco manual.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="cf2ef-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**foco de WPD \_ \_ automático**</span><span class="sxs-lookup"><span data-stu-id="cf2ef-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="cf2ef-112">Especifica o foco automático, controlado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="cf2ef-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automática de foco do WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf2ef-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="cf2ef-114">Especifica que o dispositivo deve alternar automaticamente entre macro e foco normal, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="cf2ef-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf2ef-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf2ef-115">Remarks</span></span>

<span data-ttu-id="cf2ef-116">Essa enumeração é usada pela propriedade [ \_ modo de \_ \_ foco de \_ imagem do WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="cf2ef-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf2ef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf2ef-117">Requirements</span></span>



| <span data-ttu-id="cf2ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf2ef-118">Requirement</span></span> | <span data-ttu-id="cf2ef-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf2ef-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2ef-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf2ef-120">Header</span></span><br/> | <dl> <span data-ttu-id="cf2ef-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf2ef-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf2ef-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf2ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf2ef-123">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="cf2ef-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




