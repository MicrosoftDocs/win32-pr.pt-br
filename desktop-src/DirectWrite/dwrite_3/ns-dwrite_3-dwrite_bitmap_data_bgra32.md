---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Representa dados de bitmap no formato BGRA32.
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 813f3601cac03dcf477fa40f6db5105e075029ab
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548921"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>Estrutura de DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)

Representa dados de bitmap no formato BGRA32.

> [!IMPORTANT]
> Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma. Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](../dwritecore-overview.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Membros

`width`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

A largura, em pixels, do bitmap.


`height`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

A altura, em pixels, do bitmap.


`pixels`

Tipo: \_ \_ tamanho \_ do campo (largura * altura)**[UINT32](../../winprog/windows-data-types.md)\***

Um ponteiro para o local dos valores de bits para o bitmap.


## <a name="examples"></a>Exemplos

Consulte o tópico [visão geral do DWriteCore](../dwritecore-overview.md) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, reunião do projeto [aplicativos Win32] |
| **Cabeçalho** | dwrite_3. h (incluir dwrite_core. h) |