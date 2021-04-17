---
description: Especifica a relação de herança para um serviço.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: Enumeração de WPD_SERVICE_INHERITANCE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790600"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="90107-103">\_Enumeração de \_ tipos de herança de serviço WPD \_</span><span class="sxs-lookup"><span data-stu-id="90107-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="90107-104">O tipo de enumeração de **\_ tipos de \_ herança \_ de serviço WPD** especifica a relação de herança para um serviço.</span><span class="sxs-lookup"><span data-stu-id="90107-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="90107-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90107-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="90107-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="90107-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90107-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implementação de \_ herança de serviço WPD \_**</span><span class="sxs-lookup"><span data-stu-id="90107-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="90107-108">O serviço herda implementando uma definição de serviço abstrata.</span><span class="sxs-lookup"><span data-stu-id="90107-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90107-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90107-109">Requirements</span></span>



| <span data-ttu-id="90107-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="90107-110">Requirement</span></span> | <span data-ttu-id="90107-111">Valor</span><span class="sxs-lookup"><span data-stu-id="90107-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="90107-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90107-112">Header</span></span><br/> | <dl> <span data-ttu-id="90107-113"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="90107-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90107-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="90107-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90107-115">**IPortableDeviceServiceCapabilities:: getherdservices**</span><span class="sxs-lookup"><span data-stu-id="90107-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




