---
description: Fecha o banco de dados shim inicializado usando a função SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Função SdbReleaseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 82a7cf785927a5ef14e3e033c29233afcc4a49cf89d610757d110583bce4eff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815326"
---
# <a name="sdbreleasedatabase-function"></a>Função SdbReleaseDatabase

Fecha o banco de dados shim inicializado usando a [**função SdbInitDatabase.**](sdbinitdatabase.md)

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSDB* \[ Em\]
</dt> <dd>

Um handle para o banco de dados shim retornado pela [**função SdbInitDatabase.**](sdbinitdatabase.md)

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

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




