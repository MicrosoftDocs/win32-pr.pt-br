---
title: Enumeração de DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: A \_ enumeração de DataType attr do DRM \_ define os tipos de dados usados para atributos e propriedades DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Formato de mídia do Windows de enumeração de DRM_ATTR_DATATYPE
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110526"
---
# <a name="drm_attr_datatype-enumeration"></a>\_Enumeração de \_ tipo de dados attr DRM

A enumeração de **\_ \_ DataType attr do DRM** define os tipos de dados usados para atributos e propriedades DRM.

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**tipo de DRM \_ \_ DWORD**
</dt> <dd>

A propriedade é um valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**Cadeia de caracteres do \_ tipo DRM \_**
</dt> <dd>

A propriedade é uma cadeia de caracteres Unicode terminada em nulo.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**tipo de DRM \_ \_ binário**
</dt> <dd>

A propriedade é uma matriz de bytes.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**tipo de DRM \_ \_ bool**
</dt> <dd>

A propriedade é um valor booliano de 4 bytes.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**tipo de DRM \_ \_ QWORD**
</dt> <dd>

A propriedade é um valor **QWORD** de 8 bytes.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_palavra do tipo DRM \_**
</dt> <dd>

A propriedade é um valor de **palavra** de 2 bytes.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID do tipo DRM \_**
</dt> <dd>

A propriedade é um valor de GUID de 128 bits (6 bytes).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





