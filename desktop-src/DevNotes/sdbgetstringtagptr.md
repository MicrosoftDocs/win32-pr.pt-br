---
description: Recupera os dados de cadeia de caracteres para o TAGID especificado.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Função SdbGetStringTagPtr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e14c499b5f23f342192ad42b72f8a4c29f8312adbf6bbcb8310ee182cd457f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404425"
---
# <a name="sdbgetstringtagptr-function"></a>Função SdbGetStringTagPtr

Recupera os dados de cadeia de caracteres para o **TagId** especificado.

## <a name="syntax"></a>Sintaxe


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiWhich* \[ no\]
</dt> <dd>

O **TagId** que corresponde aos dados de cadeia de caracteres a serem recuperados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retornará um ponteiro para os dados da cadeia de caracteres ou **NULL** se **TagId** for inválido ou não for do tipo marca de tipo **\_ cadeia de \_ caracteres** ou **tipo de marca \_ \_ STRINGREF**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




