---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsula um bitmap independente de dispositivo de 32 bits e um contexto de dispositivo, que pode ser usado para renderizar glifos.
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: e12bceefd7ffb89a427edc04b4910b6346dfb066
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881815"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>Interface IDWriteBitmapRenderTarget2 (dwrite_3. h)

Encapsula um bitmap independente de dispositivo de 32 bits e um contexto de dispositivo, que pode ser usado para renderizar glifos.

> [!IMPORTANT]
> Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md). O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma. Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="inheritance"></a>Herança

A interface **IDWriteBitmapRenderTarget2** herda de [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).

## <a name="methods"></a>Métodos

A interface **IDWriteBitmapRenderTarget2** tem esses métodos.

| Método | Descrição |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2:: getbitmapdata](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Recupera os dados de pixel de um destino de renderização de bitmap. |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, reunião do projeto [aplicativos Win32] |
| **Cabeçalho** | dwrite_3. h (incluir dwrite_core. h) |