---
description: Por padrão, quando o teste de profundidade é executado em uma superfície de renderização, o sistema Direct3D atualiza a superfície de destino de renderização se o valor de profundidade correspondente (z ou w) para cada ponto for menor que o valor no buffer de profundidade.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Alterando funções de comparação de buffer de profundidade (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646540"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="4f4db-103">Alterando funções de comparação de buffer de profundidade (D3D9)</span><span class="sxs-lookup"><span data-stu-id="4f4db-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="4f4db-104">Por padrão, quando o teste de profundidade é executado em uma superfície de renderização, o sistema Direct3D atualiza a superfície de destino de renderização se o valor de profundidade correspondente (z ou w) para cada ponto for menor que o valor no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4f4db-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="4f4db-105">Em um aplicativo C++, você altera como o sistema executa comparações em valores de profundidade chamando o método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) com o parâmetro *State* definido como D3DRS \_ ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="4f4db-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="4f4db-106">O parâmetro *Value* deve ser definido como um valor no tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="4f4db-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f4db-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f4db-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f4db-108">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="4f4db-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
