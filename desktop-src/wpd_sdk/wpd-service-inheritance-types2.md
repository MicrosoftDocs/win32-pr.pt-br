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
# <a name="wpd_service_inheritance_types-enumeration"></a>\_Enumeração de \_ tipos de herança de serviço WPD \_

O tipo de enumeração de **\_ tipos de \_ herança \_ de serviço WPD** especifica a relação de herança para um serviço.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implementação de \_ herança de serviço WPD \_**
</dt> <dd>

O serviço herda implementando uma definição de serviço abstrata.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceServiceCapabilities:: getherdservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




