---
description: Localiza o primeiro registro DWORD no índice especificado que atende aos critérios especificados.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Função SdbFindFirstDWORDIndexedTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161567"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Função SdbFindFirstDWORDIndexedTag

Localiza o primeiro **registro DWORD** no índice especificado que atende aos critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tWhich* \[ Em\]
</dt> <dd>

O tipo do índice. Consulte [**TAG**](tag.md) para ver uma lista de valores.

</dd> <dt>

*tKey* \[ Em\]
</dt> <dd>

O tipo principal.

</dd> <dt>

*dwName* \[ Em\]
</dt> <dd>

O nome dos dados a serem encontrados. Esse valor será convertido em uma chave.

</dd> <dt>

*pFindInfo* \[ out\]
</dt> <dd>

Uma [**estrutura FIND \_ INFO**](find-info.md) que recebe o registro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **TAGID** da primeira combinação ou **TAG \_ NULL** se nenhuma corresponder for encontrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




