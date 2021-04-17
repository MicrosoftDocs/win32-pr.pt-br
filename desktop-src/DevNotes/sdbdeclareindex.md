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
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754901"
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

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tWhich* \[ no\]
</dt> <dd>

Esse parâmetro deve ser **uma \_ \_ lista de tipos de marca**.

</dd> <dt>

*tKey* \[ no\]
</dt> <dd>

A marca que especifica o tipo a ser usado como chave. Esse parâmetro não pode ser uma **\_ \_ lista de tipos de marca**.

</dd> <dt>

*dwEntries* \[ no\]
</dt> <dd>

O número de entradas a serem alocadas no índice.

</dd> <dt>

*bUniqueKey* \[ no\]
</dt> <dd>

Se esse parâmetro for **true**, o índice será um índice de chave exclusiva.

</dd> <dt>

*piiIndex* \[ fora\]
</dt> <dd>

A **IndexID** resultante do índice recentemente declarado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Chame essa função antes de gravar marcas no novo índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INDEXid**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




