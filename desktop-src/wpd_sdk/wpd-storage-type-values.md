---
description: O tipo de enumeração WPD \_ STORAGE TYPE VALUES descreve os diferentes tipos de armazenamento Windows dispositivo \_ \_ portátil.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: WPD_STORAGE_TYPE_VALUES enumeração (PortableDevice.h)
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
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842072"
---
# <a name="wpd_storage_type_values-enumeration"></a>Enumeração DE VALORES \_ \_ DE TIPO DE \_ ARMAZENAMENTO WPD

O **tipo de enumeração WPD \_ STORAGE TYPE \_ \_ VALUES** descreve os diferentes tipos de armazenamento Windows dispositivo portátil.

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

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**TIPO DE ARMAZENAMENTO WPD \_ \_ \_ INDEFINIDO**
</dt> <dd>

O armazenamento é de um tipo indefinido.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**TIPO DE ARMAZENAMENTO WPD \_ \_ ROM \_ \_ FIXO**
</dt> <dd>

O armazenamento não é removível e somente leitura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**ROM REMOVÍVEL DO TIPO \_ \_ DE \_ \_ ARMAZENAMENTO WPD**
</dt> <dd>

O armazenamento é removível e é somente leitura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**TIPO DE ARMAZENAMENTO WPD \_ \_ RAM \_ \_ FIXA**
</dt> <dd>

O armazenamento não é removível e é capaz de leitura/gravação.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**RAM REMOVÍVEL DO \_ \_ TIPO DE \_ \_ ARMAZENAMENTO WPD**
</dt> <dd>

O armazenamento é removível e é capaz de ler/gravar.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




