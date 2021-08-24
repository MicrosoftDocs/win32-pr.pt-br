---
description: Fecha o banco de dados especificado.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Função SdbCloseDatabaseWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0ef1c02731f2875fbdfc910243ed80faa28b6ab029314ea43ef281355a08487a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161577"
---
# <a name="sdbclosedatabasewrite-function"></a>Função SdbCloseDatabaseWrite

Fecha o banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI SdbCloseDatabaseWrite(
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

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função chama [**SdbCloseDatabase**](sdbclosedatabase.md); Portanto, essas duas funções são equivalentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> </dl>

 

 




