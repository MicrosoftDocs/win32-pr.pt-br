---
title: Enumeração de WMDM_TAG_DATATYPE
description: O \_ tipo de enumeração de DataType da marca WMDM \_ define um tipo de dados.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd725e6d8a0e1baef8a6dfc98cb5d3056f5d67b2d7babd07c919692d96248881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862666"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_Enumeração de tipo de dados de marca WMDM \_

O tipo de enumeração de **\_ \_ DataType da marca WMDM** define um tipo de dados.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**tipo de WMDM \_ \_ DWORD**
</dt> <dd>

Especifica um valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**Cadeia de caracteres do \_ tipo WMDM \_**
</dt> <dd>

Especifica uma cadeia de caracteres Unicode terminada em nulo (2 bytes por caractere).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_tipo de \_ binário do WMDM**
</dt> <dd>

Especifica uma matriz de bytes.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**tipo de WMDM \_ \_ bool**
</dt> <dd>

Especifica um valor booliano de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ tipo \_ QWORD**
</dt> <dd>

Especifica um valor **QWORD** de 8 bytes.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**tipo de WMDM \_ \_ Word**
</dt> <dd>

Especifica um valor de **palavra** de 2 bytes.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID do tipo WMDM \_**
</dt> <dd>

Especifica um GUID de 128 bits (16 bytes).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_data do tipo WMDM \_**
</dt> <dd>

Especifica uma data.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](enumeration-types.md)
</dt> </dl>

 

 





