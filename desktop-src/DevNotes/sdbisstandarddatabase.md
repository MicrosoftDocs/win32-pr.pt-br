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
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010085"
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

## <a name="return-value"></a>Retornar valor

A função retornará **true** se o GUID representar um banco de dados padrão ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




