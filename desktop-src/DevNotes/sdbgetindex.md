---
description: Recupera o índice para a marca e o tipo de chave especificados do banco de dados especificado.
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
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666471"
---
# <a name="sdbgetindex-function"></a>Função SdbGetIndex

Recupera o índice para a marca e o tipo de chave especificados do banco de dados especificado.

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

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tWhich* \[ Em\]
</dt> <dd>

A TAG.

</dd> <dt>

*tKey* \[ Em\]
</dt> <dd>

O tipo principal.

</dd> <dt>

*lpdwFlags* \[ out, opcional\]
</dt> <dd>

Esse parâmetro pode ser 0 ou **SHIMDB \_ INDEX UNIQUE \_ \_ KEY** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **TAGID** do índice ou **TAGID \_ NULL.**

## <a name="remarks"></a>Comentários

O índice resultante pode ser usado para operações de leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




