---
title: Auxiliares de HLSL
description: Para ajudar os autores de efeito na escrita de sombreadores de pixel vinculados, o d2d1effecthelpers. hlsli define um conjunto de extensões de linguagem HLSL na forma de métodos auxiliares e macros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916038"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="9d9c9-103">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="9d9c9-103">HLSL Helpers</span></span>

<span data-ttu-id="9d9c9-104">Para ajudar os autores de efeito na escrita de sombreadores de pixel vinculados, o d2d1effecthelpers. hlsli define um conjunto de extensões de linguagem HLSL na forma de métodos auxiliares e macros.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="9d9c9-105">Para adicionar o d2d1effecthelpers. hlsli ao seu projeto, adicione uma \# instrução include no arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="9d9c9-106">d2d1effecthelpers. hlsli está localizado no mesmo local que outros cabeçalhos Direct2D, como d2d1. h; Ele pode ser referenciado na página de propriedades do arquivo HLSL adicionando a macro $ (WindowsSDK \_ IncludePath) à propriedade de diretórios de inclusão adicional.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="9d9c9-107">Observe que a \# instrução include deve vir após qualquer política de pré-processador, como a \_ contagem de entrada D2D \_ ter sido definida.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="9d9c9-108">Direct2D não dá suporte à vinculação de sombreadores de computação ou de vértice.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="9d9c9-109">No entanto, se o efeito usar um sombreador de vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="9d9c9-110">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="9d9c9-110">Preprocessor Directives</span></span>

<span data-ttu-id="9d9c9-111">As diretivas de pré-processador são necessárias para comunicar informações sobre o efeito.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="9d9c9-112">Isso inclui o número de entradas e o tipo de amostragem de cada entrada.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="9d9c9-113">Os valores a seguir devem ser definidos no código do sombreador de efeito acima do ponto de entrada do sombreador relevante quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="9d9c9-114">`D2D_INPUT_COUNT <N>` : Declara o número de entradas de textura para o efeito.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="9d9c9-115">Se o efeito tiver um número variável de entradas, esse valor deverá ser definido adequadamente para cada ponto de entrada do sombreador.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="9d9c9-116">Definir esse valor é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="9d9c9-117">`D2D_INPUT<N>_SIMPLE` : Declara a entrada enésima para usar a amostragem simples.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="9d9c9-118">Se não estiver definido, a entrada enésima será complexa.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="9d9c9-119">Definir esse valor é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="9d9c9-120">`D2D_INPUT<N>_COMPLEX` : Declara a entrada enésima para usar amostragem complexa.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="9d9c9-121">Se não estiver definido, a entrada enésima será complexa.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="9d9c9-122">Definir esse valor é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="9d9c9-123">`D2D_REQUIRES_SCENE_POSITION` : Indica que a função de sombreador chama métodos auxiliares que usam o valor de posição de cena (ou seja, a função auxiliar [D2DGetScenePosition](d2dgetsceneposition.md) ).</span><span class="sxs-lookup"><span data-stu-id="9d9c9-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="9d9c9-124">Esse parâmetro só deve ser incluído quando necessário, já que apenas uma função por sombreador vinculado pode utilizar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="9d9c9-125">Definir esse valor é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="9d9c9-126">`D2D_CUSTOM_ENTRY` : Indica que a função de sombreador de pixel consome a saída de um sombreador de vértice personalizado e, portanto, irá declarar seus parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="9d9c9-127">Todas as entradas de sombreador de vértice personalizadas usam amostragem complexa e não podem consumir a saída de outra função de sombreador (ou seja, elas são somente pós-link).</span><span class="sxs-lookup"><span data-stu-id="9d9c9-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="9d9c9-128">Definir esse valor é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-128">Defining this value is optional.</span></span>

<span data-ttu-id="9d9c9-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9d9c9-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="9d9c9-130">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="9d9c9-130">Helper Functions</span></span>

<span data-ttu-id="9d9c9-131">As funções auxiliares são usadas como substituição para algumas funções intrínsecas HLSL nativas.</span><span class="sxs-lookup"><span data-stu-id="9d9c9-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="9d9c9-132">No momento da compilação, essas funções auxiliares são redefinidas pelo Direct2D para a versão apropriada, dependendo do tipo de destino de compilação (sombreador completo ou função de exportação).</span><span class="sxs-lookup"><span data-stu-id="9d9c9-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="9d9c9-133">As funções auxiliares:</span><span class="sxs-lookup"><span data-stu-id="9d9c9-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="9d9c9-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="9d9c9-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="9d9c9-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="9d9c9-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="9d9c9-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="9d9c9-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="9d9c9-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="9d9c9-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="9d9c9-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="9d9c9-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="9d9c9-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="9d9c9-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="9d9c9-140">\_Entrada do PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="9d9c9-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="9d9c9-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d9c9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d9c9-142">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="9d9c9-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




