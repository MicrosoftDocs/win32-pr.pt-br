---
description: Declara um novo índice no banco de dados especificado.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Função SdbDeclareIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666585"
---
# <a name="sdbdeclareindex-function"></a>Função SdbDeclareIndex

Declara um novo índice no banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
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

Esse parâmetro deve ser **TAG \_ TYPE \_ LIST.**

</dd> <dt>

*tKey* \[ Em\]
</dt> <dd>

A TAG que especifica o tipo a ser usado como a chave. Esse parâmetro não pode ser **TAG \_ TYPE \_ LIST.**

</dd> <dt>

*dwEntries* \[ Em\]
</dt> <dd>

O número de entradas a alocar no índice.

</dd> <dt>

*bUniqueKey* \[ Em\]
</dt> <dd>

Se esse parâmetro for **TRUE,** o índice será um índice de chave exclusiva.

</dd> <dt>

*piiIndex* \[ out\]
</dt> <dd>

O **INDEXID resultante** do índice recém-declarado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="remarks"></a>Comentários

Chame essa função antes de escrever marcas no novo índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




