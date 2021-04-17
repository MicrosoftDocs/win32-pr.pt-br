---
description: Contém informações de contexto de pesquisa.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Estrutura de FIND_INFO
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
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752926"
---
# <a name="find_info-structure"></a>LOCALIZAR \_ estrutura de informações

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

O **TagId** para o índice a ser pesquisado.

</dd> <dt>

**tiCurrent**
</dt> <dd>

O **TagId** para o item atual que estava localizado.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

O **TagId** para o último registro após FindFirst se o índice for exclusivo.

</dd> <dt>

**tName**
</dt> <dd>

O tipo do item a ser localizado. Consulte [tipos de marca](tag-types.md).

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Um contador interno usado para controlar onde deve iniciar a próxima operação Localizar.

</dd> <dt>

**dwFlags**
</dt> <dd>

Esse membro pode ser 0 ou **SHIMDB \_ \_ \_ chave exclusiva de índice** (0x00000001), que indica que se trata de um índice de chave exclusiva.

</dd> <dt>

**ullKey**
</dt> <dd>

A chave para a entrada atual.

</dd> <dt>

**szName**
</dt> <dd>

A cadeia de caracteres atual (se o tipo de marca for **tipo de marca \_ \_ STRINGREF**).

</dd> <dt>

**dwName**
</dt> <dd>

O valor **DWORD** atual (se o tipo de marca for **marca \_ tipo \_ DWORD**).

</dd> <dt>

**pguidName**
</dt> <dd>

O valor de GUID atual (se o tipo de marca for **marca \_ tipo \_ binário** e a marca for **\_ \_ ID do banco de dados de marca**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




