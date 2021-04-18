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
ms.openlocfilehash: ea60bbd4933cd890321e0caeb095778922699a46
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105798329"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="eb1b6-103">Estrutura de DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="eb1b6-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="eb1b6-104">Representa dados de bitmap no formato BGRA32.</span><span class="sxs-lookup"><span data-stu-id="eb1b6-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb1b6-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="eb1b6-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="eb1b6-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="eb1b6-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="eb1b6-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="eb1b6-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1b6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb1b6-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="eb1b6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="eb1b6-109">Members</span></span>

`width`

<span data-ttu-id="eb1b6-110">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1b6-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1b6-111">A largura, em pixels, do bitmap.</span><span class="sxs-lookup"><span data-stu-id="eb1b6-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="eb1b6-112">Tipo: **[UINT32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1b6-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1b6-113">A altura, em pixels, do bitmap.</span><span class="sxs-lookup"><span data-stu-id="eb1b6-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="eb1b6-114">Tipo: \_ \_ tamanho \_ do campo (largura \* altura)**[UINT32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb1b6-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb1b6-115">Um ponteiro para o local dos valores de bits para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="eb1b6-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="eb1b6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb1b6-116">Examples</span></span>

<span data-ttu-id="eb1b6-117">Consulte o tópico [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="eb1b6-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1b6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb1b6-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="eb1b6-119">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="eb1b6-119">**Minimum supported client**</span></span> | <span data-ttu-id="eb1b6-120">Windows 10, versão 0,1 de pré-lançamento do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="eb1b6-120">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="eb1b6-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="eb1b6-121">**Header**</span></span> | <span data-ttu-id="eb1b6-122">dwrite_3. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="eb1b6-122">dwrite_3.h (include dwrite_core.h)</span></span> |