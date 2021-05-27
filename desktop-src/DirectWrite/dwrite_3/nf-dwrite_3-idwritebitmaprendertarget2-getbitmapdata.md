---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Recupera os dados de pixel de um destino de renderização de bitmap.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550281"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>Método IDWriteBitmapRenderTarget2:: getbitmapdata (dwrite_3. h)

Recupera os dados de pixel de um destino de renderização de bitmap.

> [!IMPORTANT]
> Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma. Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](../dwritecore-overview.md).

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parâmetros

`bitmapData`

Tipo: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Um ponteiro para os dados de pixel.

## <a name="return-value"></a>Retornar valor

Tipo: <b>HRESULT</b>

Se esse método tiver sucesso, ele retornará <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Caso contrário, ele retorna um código de erro <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Exemplos

Consulte o tópico [visão geral do DWriteCore](../dwritecore-overview.md) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, reunião do projeto [aplicativos Win32] |
| **Cabeçalho** | dwrite_3. h (incluir dwrite_core. h) |
| **Biblioteca** | Dwrite. lib |
| **DLL** | Dwrite.dll |

## <a name="see-also"></a>Confira também

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)