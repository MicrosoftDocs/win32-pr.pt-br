---
description: Confirma índices recém-criados para o banco de dados especificado.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Função SdbCommitIndexes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088995"
---
# <a name="sdbcommitindexes-function"></a>Função SdbCommitIndexes

Confirma índices recém-criados para o banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ entrada, saída\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




