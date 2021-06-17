---
description: Saiba mais sobre como renderizar um efeito para o Direct3D 10. Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Renderizar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262568"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="d0f5c-104">Renderizar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-104">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="d0f5c-105">Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-105">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="d0f5c-106">Cada técnica especifica sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, estado do sombreador, estado de amostra e textura e outro estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-106">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="d0f5c-107">Portanto, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse estado criando e renderizar o efeito.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-107">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="d0f5c-108">Há algumas etapas para preparar um efeito para renderização.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-108">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="d0f5c-109">A primeira é a compilação, que verifica o código HLSL como em relação à sintaxe da linguagem HLSL e às regras da estrutura de efeito.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-109">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="d0f5c-110">Você pode compilar um efeito de seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário do compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-110">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="d0f5c-111">Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-111">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="d0f5c-112">Depois que o efeito é criado, há duas etapas restantes para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-112">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="d0f5c-113">Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-113">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="d0f5c-114">Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outros devem ser atualizados sempre que seu aplicativo chamar o loop de renderização.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-114">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="d0f5c-115">Depois que as variáveis de efeito são definidas, você diz ao runtime para renderizar o efeito aplicando uma técnica.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-115">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="d0f5c-116">Todos esses tópicos são discutidos mais detalhadamente abaixo.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-116">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="d0f5c-117">Compilar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-117">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="d0f5c-118">Criar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-118">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="d0f5c-119">Definir estado de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-119">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="d0f5c-120">Aplicar uma técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-120">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="d0f5c-121">Naturalmente, há [considerações de desempenho](d3d10-graphics-programming-guide-effects-performance.md) para usar efeitos.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-121">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="d0f5c-122">Essas considerações são, em grande parte, as mesmas se você não estiver usando um efeito.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-122">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="d0f5c-123">Coisas como minimizar a quantidade de alterações de estado ou organizar as variáveis que precisam ser atualizadas por frequência.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-123">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="d0f5c-124">Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d0f5c-124">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0f5c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0f5c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f5c-126">Efeitos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d0f5c-126">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



