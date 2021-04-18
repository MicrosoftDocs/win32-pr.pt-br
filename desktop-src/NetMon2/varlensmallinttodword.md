---
description: A função VarLenSmallIntToDword converte um inteiro pequeno de comprimento variável em um DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Função VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810154"
---
# <a name="varlensmallinttodword-function"></a>Função VarLenSmallIntToDword

A função **VarLenSmallIntToDword** converte um inteiro pequeno de comprimento variável em um **DWORD**.

## <a name="syntax"></a>Sintaxe


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valores* 
</dt> <dd>

Ponteiro para o inteiro de comprimento variável e pequeno.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Comprimento (em bytes) do comprimento variável, inteiro pequeno.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Sinalizador que indica se o inteiro pequeno de comprimento variável é alternado por byte.

</dd> <dt>

*lpDword* 
</dt> <dd>

O **DWORD** para o qual o inteiro é convertido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um ponteiro para o **DWORD**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




