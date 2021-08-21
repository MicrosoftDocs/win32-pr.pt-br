---
description: Fecha o banco de dados shim especificado.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Função SdbCloseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 06e7b493d6114b4085dcabcfd5f241413b431daa081c53fd467b100e225f486c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161587"
---
# <a name="sdbclosedatabase-function"></a>Função SdbCloseDatabase

Fecha o banco de dados shim especificado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ in, out\]
</dt> <dd>

Um alça para o banco de dados shim. Esse parâmetro não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




