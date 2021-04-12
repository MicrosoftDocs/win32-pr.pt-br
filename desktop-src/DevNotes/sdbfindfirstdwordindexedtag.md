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
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500741"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Função SdbFindFirstDWORDIndexedTag

Localiza o primeiro registro **DWORD** no índice especificado que atende aos critérios especificados.

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

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tWhich* \[ no\]
</dt> <dd>

O tipo do índice. Consulte a [**marca**](tag.md) para obter uma lista de valores.

</dd> <dt>

*tKey* \[ no\]
</dt> <dd>

O tipo principal.

</dd> <dt>

*dwName* \[ no\]
</dt> <dd>

O nome dos dados a serem encontrados. Esse valor será convertido em uma chave.

</dd> <dt>

*pFindInfo* \[ fora\]
</dt> <dd>

Uma estrutura de [**\_ informações de localização**](find-info.md) que recebe o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **TagId** da primeira correspondência ou **marca \_ NULL** se nenhuma correspondência for encontrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




