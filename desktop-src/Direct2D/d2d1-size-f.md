---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454863"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="e5fa4-104">D2D1 \_ tamanho \_ F</span><span class="sxs-lookup"><span data-stu-id="e5fa4-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="e5fa4-105">Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="e5fa4-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5fa4-106">Remarks</span></span>

<span data-ttu-id="e5fa4-107">Como pontos, os tamanhos são outro conceito de elementos gráficos importantes.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="e5fa4-108">Em Direct2D, os tamanhos são representados pelas estruturas de tamanho **\_ \_ F** ou [**d2d1 Size \_ \_ U**](d2d1-size-u.md) de d2d1.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="e5fa4-109">Ambos contêm um par ordenado de números, normalmente a largura e a altura de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="e5fa4-110">A **estrutura \_ \_ F de tamanho de d2d1** contém um par ordenado de valores **float** e a estrutura **\_ \_ U de tamanho de d2d1** contém um par ordenado de valores **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="e5fa4-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="e5fa4-111">**D2d1 \_ TAMANHO \_ f** é um novo nome para um tipo já definido **D2D \_ tamanho \_ F**.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="e5fa4-112">Para obter uma lista dos campos fornecidos pelo **tamanho de d2d1 \_ \_ f**, consulte **D2D \_ Size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="e5fa4-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fa4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5fa4-113">Requirements</span></span>



| <span data-ttu-id="e5fa4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5fa4-114">Requirement</span></span> | <span data-ttu-id="e5fa4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e5fa4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fa4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5fa4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fa4-117">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="e5fa4-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e5fa4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5fa4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fa4-119">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e5fa4-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e5fa4-120">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="e5fa4-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e5fa4-121">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="e5fa4-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="e5fa4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5fa4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5fa4-123"><dt>D2DBaseTypes. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5fa4-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e5fa4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5fa4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5fa4-125">**D2D \_ tamanho \_ F**</span><span class="sxs-lookup"><span data-stu-id="e5fa4-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="e5fa4-126">**D2D1 \_ tamanho \_ U**</span><span class="sxs-lookup"><span data-stu-id="e5fa4-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="e5fa4-127">**\_Ponto d2d1 \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="e5fa4-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

