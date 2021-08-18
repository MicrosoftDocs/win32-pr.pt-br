---
description: Determina se o banco de dados especificado é um dos bancos de dados padrão (SysMain, AppHelp, Drvmain ou Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Função SdbIsStandardDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045186"
---
# <a name="sdbisstandarddatabase-function"></a>Função SdbIsStandardDatabase

Determina se o banco de dados especificado é um dos bancos de dados padrão (SysMain, AppHelp, Drvmain ou Msimain).

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*GuidDB* \[ no\]
</dt> <dd>

O GUID do banco de dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retornará **true** se o GUID representar um banco de dados padrão ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




