---
description: Habilita a criação e modificação de índice para o banco de dados especificado.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Função SdbStartIndexing
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3643936511755642cf9997709faa69d7bb3e902e5cf3e9dd2b0f56bda681b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815266"
---
# <a name="sdbstartindexing-function"></a>Função SdbStartIndexing

Habilita a criação e modificação de índice para o banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*iiWhich* \[ Em\]
</dt> <dd>

O identificador do índice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




