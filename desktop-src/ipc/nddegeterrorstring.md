---
description: Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Função NDdeGetErrorString (Nddeapi. h)
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
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010351"
---
# <a name="nddegeterrorstring-function"></a>Função NDdeGetErrorString

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

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

*uErrorCode* \[ no\]
</dt> <dd>

O código de erro a ser convertido em uma cadeia de caracteres de erro.

</dd> <dt>

*lpszErrorString* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe a cadeia de caracteres de erro traduzida. Este parâmetro não pode ser **nulo**. Se o buffer não for grande o suficiente para armazenar a cadeia de caracteres de erro completa, a cadeia de caracteres será truncada.

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho do buffer para receber a cadeia de caracteres de erro, em **TCHARs**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função obtiver êxito, o valor retornado será zero.

Se a função falhar, o valor de retorno será um código de erro diferente de zero. Se o buffer *lpszErrorString* não for grande o suficiente para aceitar a cadeia de caracteres de erro completa e a cadeia de caracteres estiver truncada, a função retornará o valor NDDE \_ \_ erro interno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> </dl>

 

 




