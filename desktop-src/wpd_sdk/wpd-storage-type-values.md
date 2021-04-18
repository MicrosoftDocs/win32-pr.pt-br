---
description: O \_ tipo de enumeração de valores de tipo de armazenamento WPD \_ \_ descreve os diferentes tipos de armazenamento de dispositivo portátil do Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumeração de WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752759"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_Enumeração de \_ valores de tipo de armazenamento WPD \_

O tipo de enumeração de **\_ valores de \_ tipo \_ de armazenamento WPD** descreve os diferentes tipos de armazenamento de dispositivo portátil do Windows.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_tipo de armazenamento WPD \_ \_ indefinido**
</dt> <dd>

O armazenamento é de um tipo indefinido.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_ \_ ROM fixa de tipo de armazenamento WPD \_ \_**
</dt> <dd>

O armazenamento não é removível e somente leitura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ \_ ROM removível de tipo de armazenamento WPD \_**
</dt> <dd>

O armazenamento é removível e é somente leitura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ RAM fixa de tipo de armazenamento WPD \_ \_**
</dt> <dd>

O armazenamento não é removível e é compatível com leitura/gravação.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ RAM removível de tipo de armazenamento WPD \_**
</dt> <dd>

O armazenamento é removível e é compatível com leitura/gravação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




