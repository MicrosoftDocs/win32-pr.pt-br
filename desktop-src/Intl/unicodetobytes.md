---
UID: ''
title: Função UnicodeToBytes
description: Converte caracteres Unicode em GB18030 bytes.
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
ms.openlocfilehash: 01109763644dc04aeb398e5fc64e221cd5f3d18870df2654fa5348bc163a277c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764717"
---
# <a name="unicodetobytes-function"></a>Função UnicodeToBytes

## <a name="description"></a>Descrição

Preterido. Converte caracteres Unicode em GB18030 bytes.

**Observação**  Ao converter caracteres Unicode em GB18030 bytes, um aplicativo a ser executado no Windows Vista e posterior deve usar a [função WideCharToMultiByte.](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

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

Ponteiro para o buffer multibyte de destino.
Se *lpMultiByteStr* for 0, a contagem de byte do resultado GB18030 será retornada e nenhuma conversão será feita.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Contagem de byte do buffer multibyte de destino.
Se *cchMultiByte* for 0, a contagem de byte do resultado GB18030 será retornada e nenhuma conversão será feita.

## <a name="returns"></a>Retornos

Retorna a contagem de byte dos caracteres multibyte gerados, se bem-sucedidos.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
