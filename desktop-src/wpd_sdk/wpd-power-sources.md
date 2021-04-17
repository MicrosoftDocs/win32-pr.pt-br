---
description: O \_ tipo de enumeração de fontes de energia WPD \_ descreve a fonte de energia que um dispositivo está usando.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumeração de WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749913"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="61b86-103">Enumeração de fontes de \_ energia WPD \_</span><span class="sxs-lookup"><span data-stu-id="61b86-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="61b86-104">O tipo de enumeração de **\_ \_ fontes de energia WPD** descreve a fonte de energia que um dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="61b86-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61b86-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="61b86-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="61b86-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61b86-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_bateria de \_ fonte de energia WPD \_**</span><span class="sxs-lookup"><span data-stu-id="61b86-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="61b86-108">A fonte de energia do dispositivo é uma bateria.</span><span class="sxs-lookup"><span data-stu-id="61b86-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="61b86-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_fonte de energia WPD \_ \_ externa**</span><span class="sxs-lookup"><span data-stu-id="61b86-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="61b86-110">O dispositivo usa uma fonte de energia externa.</span><span class="sxs-lookup"><span data-stu-id="61b86-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61b86-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="61b86-111">Remarks</span></span>

<span data-ttu-id="61b86-112">Essa enumeração é usada pela propriedade [ \_ fonte de \_ energia \_ do dispositivo WPD](device-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="61b86-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b86-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b86-113">Requirements</span></span>



| <span data-ttu-id="61b86-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b86-114">Requirement</span></span> | <span data-ttu-id="61b86-115">Valor</span><span class="sxs-lookup"><span data-stu-id="61b86-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b86-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61b86-116">Header</span></span><br/> | <dl> <span data-ttu-id="61b86-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b86-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b86-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="61b86-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b86-119">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="61b86-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




