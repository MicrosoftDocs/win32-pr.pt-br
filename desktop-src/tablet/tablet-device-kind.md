---
description: Indica o tipo de dispositivo tablet, como uma caneta, um mouse ou um digitalizador sensível ao toque.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Enumeração de TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782209"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="a672f-103">Enumeração de tipo de \_ dispositivo tablet \_</span><span class="sxs-lookup"><span data-stu-id="a672f-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="a672f-104">Indica o tipo de dispositivo tablet, como uma caneta, um mouse ou um digitalizador sensível ao toque.</span><span class="sxs-lookup"><span data-stu-id="a672f-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a672f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a672f-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="a672f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a672f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a672f-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse de dispositivo \_ do Tablet**</span><span class="sxs-lookup"><span data-stu-id="a672f-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="a672f-108">O Tablet é um mouse.</span><span class="sxs-lookup"><span data-stu-id="a672f-108">The tablet is a mouse.</span></span> <span data-ttu-id="a672f-109">Isso inclui touchpads encontrados em muitos computadores laptop.</span><span class="sxs-lookup"><span data-stu-id="a672f-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="a672f-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_caneta do dispositivo do Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="a672f-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="a672f-111">O Tablet utiliza uma caneta eletromagnética e um digitalizador.</span><span class="sxs-lookup"><span data-stu-id="a672f-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="a672f-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_toque no dispositivo do Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="a672f-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="a672f-113">O Tablet utiliza um digitalizador sensível ao toque.</span><span class="sxs-lookup"><span data-stu-id="a672f-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a672f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a672f-114">Requirements</span></span>



| <span data-ttu-id="a672f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a672f-115">Requirement</span></span> | <span data-ttu-id="a672f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a672f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a672f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a672f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a672f-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a672f-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a672f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a672f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a672f-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a672f-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="a672f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a672f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a672f-122">**Método ITablet2:: GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="a672f-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




