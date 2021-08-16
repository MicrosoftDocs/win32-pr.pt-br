---
description: Contém informações de contexto de pesquisa.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1ee5eb66928322019a455c78d71abf5461e56b1296ae79d94b83c40c2d45379e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404779"
---
# <a name="find_info-structure"></a>Estrutura FIND \_ INFO

Contém informações de contexto de pesquisa.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**tiIndex**
</dt> <dd>

O **TAGID** do índice a ser pesquisado.

</dd> <dt>

**tiCurrent**
</dt> <dd>

O **TAGID** do item atual que foi localizado.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

O **TAGID** do último registro após FindFirst se o índice for UNIQUE.

</dd> <dt>

**tName**
</dt> <dd>

O tipo do item a ser localizado. Consulte [Tipos de MARCA](tag-types.md).

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Um contador interno usado para rastrear em que local no índice a próxima operação de localizar deve iniciar.

</dd> <dt>

**dwFlags**
</dt> <dd>

Esse membro pode ser 0 ou **SHIMDB \_ INDEX UNIQUE \_ \_ KEY** (0x00000001), o que indica que esse é um índice de chave exclusiva.

</dd> <dt>

**ullKey**
</dt> <dd>

A chave para a entrada atual.

</dd> <dt>

**Szname**
</dt> <dd>

A cadeia de caracteres atual (se o tipo de marca for **TAG \_ TYPE \_ STRINGREF**).

</dd> <dt>

**dwName**
</dt> <dd>

O valor **DWORD** atual (se o tipo de marca for **TAG TYPE \_ \_ DWORD**).

</dd> <dt>

**pguidName**
</dt> <dd>

O valor guid atual (se o tipo de marca for **TAG \_ TYPE \_ BINARY** e TAG for **TAG DATABASE \_ \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




