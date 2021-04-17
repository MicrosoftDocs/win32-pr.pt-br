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
# <a name="wpd_cropped_status_values-enumeration"></a>\_Enumeração de \_ valores de status CORTADOs WPD \_

O tipo de enumeração **\_ \_ \_ valores de status cortados WPD** descreve o status de corte de uma imagem.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_status recortado WPD \_ \_ não \_ cortado**
</dt> <dd>

A imagem não foi cortada.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_status cortado \_ WPD \_ cortado**
</dt> <dd>

A imagem foi cortada.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**o \_ status recortado de WPD \_ \_ \_ não deve \_ ser \_ cortado**
</dt> <dd>

A imagem não foi e não deve ser cortada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o status cortado de uma imagem. Essa enumeração é usada pela propriedade [de \_ \_ \_ status cortada de imagem WPD](image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




