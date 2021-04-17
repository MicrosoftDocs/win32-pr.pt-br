---
description: Encerra as operações de gravação da lista especificada.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Função SdbEndWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762861"
---
# <a name="sdbendwritelisttag-function"></a>Função SdbEndWriteListTag

Encerra as operações de gravação da lista especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ entrada, saída\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiList* \[ no\]
</dt> <dd>

O [**TagId**](tagid.md) da lista

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Chame essa função depois de gravar todas as entradas da lista; Ele marcará o final da lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




