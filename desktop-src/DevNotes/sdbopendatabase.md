---
description: Abre o banco de dados de shims especificado.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Função SdbOpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646238"
---
# <a name="sdbopendatabase-function"></a>Função SdbOpenDatabase

Abre o banco de dados de shims especificado.

## <a name="syntax"></a>Sintaxe


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszPath* \[ no\]
</dt> <dd>

O caminho do banco de dados. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*ETYPE* \[ no\]
</dt> <dd>

O tipo de caminho. Consulte [**\_ tipo de caminho**](path-type.md) para obter uma lista de valores.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um identificador para o banco de dados de Shim.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




