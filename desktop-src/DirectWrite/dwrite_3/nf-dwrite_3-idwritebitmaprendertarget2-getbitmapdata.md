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
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105798330"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="58f40-103">Método IDWriteBitmapRenderTarget2:: getbitmapdata (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="58f40-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="58f40-104">Recupera os dados de pixel de um destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="58f40-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58f40-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="58f40-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="58f40-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="58f40-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="58f40-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="58f40-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="58f40-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58f40-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="58f40-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58f40-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="58f40-110">Tipo: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="58f40-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="58f40-111">Um ponteiro para os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="58f40-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="58f40-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58f40-112">Return value</span></span>

<span data-ttu-id="58f40-113">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="58f40-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="58f40-114">Se esse método tiver sucesso, ele retornará <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="58f40-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="58f40-115">Caso contrário, ele retorna um código de erro <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="58f40-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="58f40-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58f40-116">Examples</span></span>

<span data-ttu-id="58f40-117">Consulte o tópico [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="58f40-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f40-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f40-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="58f40-119">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="58f40-119">**Minimum supported client**</span></span> | <span data-ttu-id="58f40-120">Windows 10, versão 0,1 de pré-lançamento do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="58f40-120">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="58f40-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="58f40-121">**Header**</span></span> | <span data-ttu-id="58f40-122">dwrite_3. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="58f40-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="58f40-123">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="58f40-123">**Library**</span></span> | <span data-ttu-id="58f40-124">Dwrite. lib</span><span class="sxs-lookup"><span data-stu-id="58f40-124">Dwrite.lib</span></span> |
| <span data-ttu-id="58f40-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="58f40-125">**DLL**</span></span> | <span data-ttu-id="58f40-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="58f40-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="58f40-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="58f40-127">See also</span></span>

[<span data-ttu-id="58f40-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="58f40-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)