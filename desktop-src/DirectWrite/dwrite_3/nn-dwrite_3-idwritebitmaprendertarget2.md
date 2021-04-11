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
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172431"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="71b18-103">Interface IDWriteBitmapRenderTarget2 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="71b18-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="71b18-104">Encapsula um bitmap independente de dispositivo de 32 bits e um contexto de dispositivo, que pode ser usado para renderizar glifos.</span><span class="sxs-lookup"><span data-stu-id="71b18-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71b18-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="71b18-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="71b18-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="71b18-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="71b18-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="71b18-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="inheritance"></a><span data-ttu-id="71b18-108">Herança</span><span class="sxs-lookup"><span data-stu-id="71b18-108">Inheritance</span></span>

<span data-ttu-id="71b18-109">A interface **IDWriteBitmapRenderTarget2** herda de [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span><span class="sxs-lookup"><span data-stu-id="71b18-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="71b18-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="71b18-110">Methods</span></span>

<span data-ttu-id="71b18-111">A interface **IDWriteBitmapRenderTarget2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="71b18-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="71b18-112">Método</span><span class="sxs-lookup"><span data-stu-id="71b18-112">Method</span></span> | <span data-ttu-id="71b18-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="71b18-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="71b18-114">IDWriteBitmapRenderTarget2:: getbitmapdata</span><span class="sxs-lookup"><span data-stu-id="71b18-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="71b18-115">Recupera os dados de pixel de um destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="71b18-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="71b18-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71b18-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="71b18-117">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="71b18-117">**Minimum supported client**</span></span> | <span data-ttu-id="71b18-118">Windows 10, versão 0,1 de pré-lançamento do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="71b18-118">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="71b18-119">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="71b18-119">**Header**</span></span> | <span data-ttu-id="71b18-120">dwrite_3. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="71b18-120">dwrite_3.h (include dwrite_core.h)</span></span> |