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
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045156"
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

## <a name="return-value"></a>Valor retornado

A função retorna um identificador para o banco de dados de detalhes de AppHelp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




