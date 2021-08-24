---
description: Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Função NDdeGetErrorString (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 728ccd283f0f65caafd6f23781bd75f18e9c796ad2fb147f00ab6350c53bfd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557036"
---
# <a name="nddegeterrorstring-function"></a>Função NDdeGetErrorString

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uErrorCode* \[ Em\]
</dt> <dd>

O código de erro a ser convertido em uma cadeia de caracteres de erro.

</dd> <dt>

*lpszErrorString* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe a cadeia de caracteres de erro traduzida. Esse parâmetro não pode ser **NULL.** Se o buffer não for grande o suficiente para armazenar a cadeia de caracteres de erro completa, a cadeia de caracteres será truncada.

</dd> <dt>

*cBufSize* \[ Em\]
</dt> <dd>

O tamanho do buffer para receber a cadeia de caracteres de erro, em **TCHARs.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função obtiver êxito, o valor retornado será zero.

Se a função falhar, o valor de retorno será um código de erro não zero. Se o buffer *lpszErrorString* não for grande o suficiente para aceitar a cadeia de caracteres de erro completa e a cadeia de caracteres for truncada, a função retornará o valor NDDE \_ INTERNAL \_ ERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> </dl>

 

 




