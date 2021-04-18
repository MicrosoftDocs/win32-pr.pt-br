---
description: Um efeito é criado carregando-o na estrutura de efeitos.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Criar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760058"
---
# <a name="create-an-effect-direct3d-10"></a><span data-ttu-id="cd304-103">Criar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="cd304-103">Create an Effect (Direct3D 10)</span></span>

<span data-ttu-id="cd304-104">Um efeito é criado carregando-o na estrutura de efeitos.</span><span class="sxs-lookup"><span data-stu-id="cd304-104">An effect is created by loading it into the effects framework.</span></span> <span data-ttu-id="cd304-105">Se o efeito nunca tiver sido compilado, ele será compilado quando for criado.</span><span class="sxs-lookup"><span data-stu-id="cd304-105">If the effect has never been compiled, it will be compiled when it is created.</span></span> <span data-ttu-id="cd304-106">Os efeitos que já estão carregados na memória podem ser criados chamando [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="cd304-106">Effects that are already loaded into memory can be created by calling [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span></span> <span data-ttu-id="cd304-107">O exemplo de código a seguir usa [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) para criar um efeito de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="cd304-107">The following code example uses [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) to create an effect from a file.</span></span>


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



<span data-ttu-id="cd304-108">A leitura de um efeito requer os mesmos parâmetros que a compilação de um efeito, além de um dispositivo e um pool.</span><span class="sxs-lookup"><span data-stu-id="cd304-108">Reading an effect requires the same parameters as compiling an effect, plus a device and a pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd304-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd304-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd304-110">Renderizando um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="cd304-110">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



