---
description: Cria um novo banco de dados de Shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Função SdbCreateDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920345"
---
# <a name="sdbcreatedatabase-function"></a>Função SdbCreateDatabase

Cria um novo banco de dados de Shim.

## <a name="syntax"></a>Sintaxe


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszPath* \[ no\]
</dt> <dd>

O caminho em que o banco de dados deve ser salvo. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*ETYPE* \[ no\]
</dt> <dd>

O tipo de caminho. Consulte [**\_ tipo de caminho**](path-type.md) para obter uma lista de valores.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um identificador para o banco de dados Shim ou **nulo** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




