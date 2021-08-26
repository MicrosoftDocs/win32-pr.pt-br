---
Description: Recupera a cadeia de caracteres para o TAGID especificado.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Função SdbReadStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8f8652e944328298b7cd3888fa93c41d3551ba913f4acd848f60fa053ed0067e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044936"
---
# <a name="sdbreadstringtag-function"></a>Função SdbReadStringTag

Recupera a cadeia de caracteres para o **TAGID especificado.**

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tiWhich* \[ Em\]
</dt> <dd>

O **TAGID** que corresponde aos dados a serem recuperados.

</dd> <dt>

*pwszBuffer* \[ out\]
</dt> <dd>

O buffer que recebe a cadeia de caracteres. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*cchBufferSize* \[ Em\]
</dt> <dd>

O tamanho do *buffer pwszBuffer,* em caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadBinaryTag**](sdbreadbinarytag.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> </dl>

 

 




