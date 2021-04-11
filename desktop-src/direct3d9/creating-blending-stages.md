---
description: Um estágio de mesclagem é um conjunto de operações de textura e seus argumentos que definem como as texturas são combinadas.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Criando estágios de mesclagem (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089237"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="b6536-103">Criando estágios de mesclagem (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b6536-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="b6536-104">Um estágio de mesclagem é um conjunto de operações de textura e seus argumentos que definem como as texturas são combinadas.</span><span class="sxs-lookup"><span data-stu-id="b6536-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="b6536-105">Ao fazer um estágio de mesclagem, os aplicativos C++ invocam o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="b6536-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="b6536-106">A primeira chamada especifica a operação que é executada.</span><span class="sxs-lookup"><span data-stu-id="b6536-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="b6536-107">Duas invocações adicionais definem os argumentos aos quais a operação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="b6536-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="b6536-108">O exemplo de código a seguir ilustra a criação de um estágio de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b6536-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="b6536-109">Os dados de Texel em texturas contêm valores de cor e alfa.</span><span class="sxs-lookup"><span data-stu-id="b6536-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="b6536-110">Os aplicativos podem definir operações separadas para valores de cor e alfa em um único estágio de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b6536-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="b6536-111">Cada operação, cor e alfa têm seus próprios argumentos.</span><span class="sxs-lookup"><span data-stu-id="b6536-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="b6536-112">Para obter detalhes, consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="b6536-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="b6536-113">Embora não faça parte da API do Direct3D, você pode inserir as macros a seguir em seu aplicativo para abreviar o código necessário para criar estágios de mesclagem de textura.</span><span class="sxs-lookup"><span data-stu-id="b6536-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="b6536-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6536-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6536-115">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="b6536-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
