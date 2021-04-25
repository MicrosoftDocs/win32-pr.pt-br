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
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955049"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="34097-103">Estrutura de DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="34097-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="34097-104">Representa dados de bitmap no formato BGRA32.</span><span class="sxs-lookup"><span data-stu-id="34097-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34097-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="34097-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="34097-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="34097-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="34097-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="34097-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="34097-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34097-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="34097-109">Membros</span><span class="sxs-lookup"><span data-stu-id="34097-109">Members</span></span>

`width`

<span data-ttu-id="34097-110">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34097-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34097-111">A largura, em pixels, do bitmap.</span><span class="sxs-lookup"><span data-stu-id="34097-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="34097-112">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34097-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34097-113">A altura, em pixels, do bitmap.</span><span class="sxs-lookup"><span data-stu-id="34097-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="34097-114">Tipo: \_ \_ tamanho \_ do campo (largura \* altura)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="34097-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="34097-115">Um ponteiro para o local dos valores de bits para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="34097-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="34097-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34097-116">Examples</span></span>

<span data-ttu-id="34097-117">Consulte o tópico [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="34097-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="34097-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34097-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="34097-119">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="34097-119">**Minimum supported client**</span></span> | <span data-ttu-id="34097-120">Windows 10, reunião do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="34097-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="34097-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="34097-121">**Header**</span></span> | <span data-ttu-id="34097-122">dwrite_3. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="34097-122">dwrite_3.h (include dwrite_core.h)</span></span> |