---
description: Abre o banco de dados de detalhes de AppHelp especificado.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Função SdbOpenApphelpDetailsDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088812"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>Função SdbOpenApphelpDetailsDatabase

Abre o banco de dados de detalhes de AppHelp especificado.

## <a name="syntax"></a>Sintaxe


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwsDetailsDatabasePath* \[ em, opcional\]
</dt> <dd>

O caminho do banco de dados. Se esse parâmetro for **nulo**, o banco de dados do sistema local será aberto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um identificador para o banco de dados de detalhes de AppHelp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




