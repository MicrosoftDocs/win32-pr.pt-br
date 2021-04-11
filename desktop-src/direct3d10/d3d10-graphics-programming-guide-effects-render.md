---
description: Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Renderizando um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163960"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="f6a32-103">Renderizando um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="f6a32-104">Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="f6a32-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="f6a32-105">Cada técnica especifica sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, estado do sombreador, estado de amostra e textura e outro Estado de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f6a32-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="f6a32-106">Assim, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse Estado criando e renderizando o efeito.</span><span class="sxs-lookup"><span data-stu-id="f6a32-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="f6a32-107">Há algumas etapas para preparar um efeito para a renderização.</span><span class="sxs-lookup"><span data-stu-id="f6a32-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="f6a32-108">A primeira é compilar, que verifica o HLSL como código em relação à sintaxe da linguagem HLSL e às regras de estrutura de efeito.</span><span class="sxs-lookup"><span data-stu-id="f6a32-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="f6a32-109">Você pode compilar um efeito do seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário do compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="f6a32-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="f6a32-110">Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.</span><span class="sxs-lookup"><span data-stu-id="f6a32-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="f6a32-111">Depois que o efeito é criado, há duas etapas restantes para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="f6a32-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="f6a32-112">Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado.</span><span class="sxs-lookup"><span data-stu-id="f6a32-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="f6a32-113">Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outras devem ser atualizadas sempre que seu aplicativo chamar o loop de renderização.</span><span class="sxs-lookup"><span data-stu-id="f6a32-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="f6a32-114">Depois que as variáveis de efeito são definidas, você informa ao tempo de execução para renderizar o efeito aplicando uma técnica.</span><span class="sxs-lookup"><span data-stu-id="f6a32-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="f6a32-115">Esses tópicos são discutidos mais detalhadamente abaixo.</span><span class="sxs-lookup"><span data-stu-id="f6a32-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="f6a32-116">Compilar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="f6a32-117">Criar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="f6a32-118">Definir estado de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="f6a32-119">Aplicar uma técnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="f6a32-120">Naturalmente, há [considerações de desempenho](d3d10-graphics-programming-guide-effects-performance.md) para o uso de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f6a32-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="f6a32-121">Essas considerações são basicamente as mesmas se você não estiver usando um efeito.</span><span class="sxs-lookup"><span data-stu-id="f6a32-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="f6a32-122">Coisas como, minimizando a quantidade de alterações de estado ou organizando as variáveis que precisam ser atualizadas por frequência.</span><span class="sxs-lookup"><span data-stu-id="f6a32-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="f6a32-123">Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f6a32-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6a32-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6a32-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a32-125">Efeitos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6a32-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



