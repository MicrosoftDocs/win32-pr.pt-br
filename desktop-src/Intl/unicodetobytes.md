---
UID: ''
title: Função UnicodeToBytes
description: Converte caracteres Unicode em bytes GB18030.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "103639053"
---
# <a name="unicodetobytes-function"></a>Função UnicodeToBytes

## <a name="description"></a>Description

Preterido. Converte caracteres Unicode em bytes GB18030.

**Observação**  Ao converter caracteres Unicode em bytes do GB18030, um aplicativo a ser executado no Windows Vista e posterior deve usar a função [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Parâmetros

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

Ponteiro para a cadeia de caracteres Unicode a ser convertida.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Contagem de caracteres da cadeia de caracteres Unicode a ser convertida.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Ponteiro para o buffer de multibyte de destino.
Se *lpMultiByteStr* for 0, a contagem de bytes do resultado GB18030 será retornada e nenhuma conversão será feita.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Contagem de bytes do buffer de multibyte de destino.
Se *cchMultiByte* for 0, a contagem de bytes do resultado GB18030 será retornada e nenhuma conversão será feita.

## <a name="returns"></a>Retornos

Retorna a contagem de bytes dos caracteres multibyte gerados, se for bem-sucedido.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
