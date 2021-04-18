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
# <a name="tablet_device_kind-enumeration"></a>Enumeração de tipo de \_ dispositivo tablet \_

Indica o tipo de dispositivo tablet, como uma caneta, um mouse ou um digitalizador sensível ao toque.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse de dispositivo \_ do Tablet**
</dt> <dd>

O Tablet é um mouse. Isso inclui touchpads encontrados em muitos computadores laptop.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_caneta do dispositivo do Tablet \_**
</dt> <dd>

O Tablet utiliza uma caneta eletromagnética e um digitalizador.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_toque no dispositivo do Tablet \_**
</dt> <dd>

O Tablet utiliza um digitalizador sensível ao toque.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ITablet2:: GetDeviceKind**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




