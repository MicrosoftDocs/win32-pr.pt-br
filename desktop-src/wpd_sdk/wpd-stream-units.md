---
description: A \_ enumeração de unidades de fluxo WPD \_ especifica os tipos de unidade a serem usados para operações IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Enumeração de WPD_STREAM_UNITS (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662934"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="f72da-103">Enumeração de unidades de \_ fluxo WPD \_</span><span class="sxs-lookup"><span data-stu-id="f72da-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="f72da-104">A enumeração de **\_ \_ unidades de fluxo WPD** especifica os tipos de unidade a serem usados para operações [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .</span><span class="sxs-lookup"><span data-stu-id="f72da-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f72da-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="f72da-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f72da-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f72da-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_bytes de \_ unidades de fluxo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f72da-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="f72da-108">As unidades de fluxo são especificadas em bytes.</span><span class="sxs-lookup"><span data-stu-id="f72da-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f72da-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_quadros de \_ unidades de fluxo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f72da-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="f72da-110">As unidades de fluxo são especificadas em quadros.</span><span class="sxs-lookup"><span data-stu-id="f72da-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="f72da-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_linhas de \_ unidades de fluxo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f72da-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="f72da-112">As unidades de fluxo são especificadas em linhas.</span><span class="sxs-lookup"><span data-stu-id="f72da-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="f72da-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**\_ \_ milissegundos de unidades de fluxo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f72da-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="f72da-114">As unidades de fluxo são especificadas em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f72da-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f72da-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_ \_ microssegundos de unidades de fluxo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f72da-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="f72da-116">As unidades de fluxo são especificadas em microssegundos.</span><span class="sxs-lookup"><span data-stu-id="f72da-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f72da-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72da-117">Requirements</span></span>



| <span data-ttu-id="f72da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72da-118">Requirement</span></span> | <span data-ttu-id="f72da-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f72da-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72da-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f72da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f72da-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f72da-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f72da-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f72da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f72da-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f72da-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="f72da-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f72da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f72da-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72da-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f72da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72da-127">**IPortableDeviceUnitsStream**</span><span class="sxs-lookup"><span data-stu-id="f72da-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="f72da-128">**IPortableDeviceUnitsStream::SeekInUnits**</span><span class="sxs-lookup"><span data-stu-id="f72da-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




