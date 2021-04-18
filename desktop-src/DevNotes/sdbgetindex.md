---
description: Recupera o índice para a marca especificada e o tipo de chave do banco de dados especificado.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Função SdbGetIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457002"
---
# <a name="sdbgetindex-function"></a>Função SdbGetIndex

Recupera o índice para a marca especificada e o tipo de chave do banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tWhich* \[ no\]
</dt> <dd>

A marca.

</dd> <dt>

*tKey* \[ no\]
</dt> <dd>

O tipo principal.

</dd> <dt>

*lpdwFlags* \[ out, opcional\]
</dt> <dd>

Esse parâmetro pode ser 0 ou **SHIMDB \_ \_ \_ chave exclusiva do índice** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O **TagId** do índice ou **TagId \_ nulo**.

## <a name="remarks"></a>Comentários

O índice resultante pode ser usado para operações de leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




