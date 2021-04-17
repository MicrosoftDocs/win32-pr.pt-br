---
description: O \_ tipo de \_ enumeração valores de status cortados WPD \_ descreve o status de corte de uma imagem.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Enumeração de WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754223"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="55b5c-103">\_Enumeração de \_ valores de status CORTADOs WPD \_</span><span class="sxs-lookup"><span data-stu-id="55b5c-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="55b5c-104">O tipo de enumeração **\_ \_ \_ valores de status cortados WPD** descreve o status de corte de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="55b5c-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55b5c-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="55b5c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="55b5c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="55b5c-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_status recortado WPD \_ \_ não \_ cortado**</span><span class="sxs-lookup"><span data-stu-id="55b5c-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="55b5c-108">A imagem não foi cortada.</span><span class="sxs-lookup"><span data-stu-id="55b5c-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="55b5c-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_status cortado \_ WPD \_ cortado**</span><span class="sxs-lookup"><span data-stu-id="55b5c-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="55b5c-110">A imagem foi cortada.</span><span class="sxs-lookup"><span data-stu-id="55b5c-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="55b5c-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**o \_ status recortado de WPD \_ \_ \_ não deve \_ ser \_ cortado**</span><span class="sxs-lookup"><span data-stu-id="55b5c-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="55b5c-112">A imagem não foi e não deve ser cortada.</span><span class="sxs-lookup"><span data-stu-id="55b5c-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55b5c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55b5c-113">Remarks</span></span>

<span data-ttu-id="55b5c-114">Indica o status cortado de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="55b5c-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="55b5c-115">Essa enumeração é usada pela propriedade [de \_ \_ \_ status cortada de imagem WPD](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="55b5c-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b5c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b5c-116">Requirements</span></span>



| <span data-ttu-id="55b5c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b5c-117">Requirement</span></span> | <span data-ttu-id="55b5c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55b5c-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b5c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55b5c-119">Header</span></span><br/> | <dl> <span data-ttu-id="55b5c-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b5c-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b5c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="55b5c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b5c-122">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="55b5c-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




