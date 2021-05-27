---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsula um bitmap independente de dispositivo de 32 bits e o contexto do dispositivo, que pode ser usado para renderizar glifos.
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
ms.openlocfilehash: 346b2e9c7510010abb50f421489b67f7d327512f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548941"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="116c7-103">Interface IDWriteBitmapRenderTarget2 (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="116c7-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="116c7-104">Encapsula um bitmap independente de dispositivo de 32 bits e o contexto do dispositivo, que pode ser usado para renderizar glifos.</span><span class="sxs-lookup"><span data-stu-id="116c7-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="116c7-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="116c7-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="116c7-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="116c7-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="116c7-107">Para obter mais informações e exemplos de código, consulte [Visão geral de DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="116c7-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="116c7-108">Herança</span><span class="sxs-lookup"><span data-stu-id="116c7-108">Inheritance</span></span>

<span data-ttu-id="116c7-109">A interface **IDWriteBitmapRenderTarget2** herda de [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span><span class="sxs-lookup"><span data-stu-id="116c7-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="116c7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="116c7-110">Methods</span></span>

<span data-ttu-id="116c7-111">A interface **IDWriteBitmapRenderTarget2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="116c7-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="116c7-112">Método</span><span class="sxs-lookup"><span data-stu-id="116c7-112">Method</span></span> | <span data-ttu-id="116c7-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="116c7-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="116c7-114">IDWriteBitmapRenderTarget2::GetBitmapData</span><span class="sxs-lookup"><span data-stu-id="116c7-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="116c7-115">Recupera os dados de pixel de um destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="116c7-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="116c7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116c7-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="116c7-117">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="116c7-117">**Minimum supported client**</span></span> | <span data-ttu-id="116c7-118">Windows 10, Project Reunion [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="116c7-118">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="116c7-119">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="116c7-119">**Header**</span></span> | <span data-ttu-id="116c7-120">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="116c7-120">dwrite_3.h (include dwrite_core.h)</span></span> |