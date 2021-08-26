---
description: A função VarLenSmallIntToDword converte um inteiro pequeno e de comprimento variável em um DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Função VarLenSmallIntToDword (Netmon.h)
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
ms.openlocfilehash: ffec440adc903ddb9a5157e8e5f36037e092f0c4bf0cd52da79b0839220366ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962726"
---
# <a name="varlensmallinttodword-function"></a>Função VarLenSmallIntToDword

A **função VarLenSmallIntToDword** converte um inteiro pequeno e de comprimento variável em um **DWORD.**

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

*Pvalue* 
</dt> <dd>

Ponteiro para o tamanho variável, inteiro pequeno.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Comprimento (em bytes) do tamanho variável, inteiro pequeno.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Sinalizador que indica se o inteiro pequeno de comprimento variável é trocado por byte.

</dd> <dt>

*lpDword* 
</dt> <dd>

O **DWORD** no que o inteiro é convertido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um ponteiro para **o DWORD.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




