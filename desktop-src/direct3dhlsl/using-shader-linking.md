---
title: Usando vinculação de sombreador
description: Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641753"
---
# <a name="using-shader-linking"></a><span data-ttu-id="1a2ec-103">Usando vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="1a2ec-103">Using shader linking</span></span>

<span data-ttu-id="1a2ec-104">Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="1a2ec-105">A vinculação de sombreador tem suporte a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="1a2ec-106">**Objetivo:** Saiba como usar a vinculação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a2ec-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1a2ec-107">Prerequisites</span></span>

<span data-ttu-id="1a2ec-108">Partimos do princípio de que você conhece C++.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="1a2ec-109">Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="1a2ec-110">**Tempo total para conclusão:** 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="1a2ec-111">Para onde ir a partir de agora</span><span class="sxs-lookup"><span data-stu-id="1a2ec-111">Where to go from here</span></span>

<span data-ttu-id="1a2ec-112">Consulte também [APIs de compilador do HLSL](dx-graphics-d3dcompiler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ec-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="1a2ec-113">Nós lhe mostramos como:</span><span class="sxs-lookup"><span data-stu-id="1a2ec-113">We show you how to:</span></span>

-   <span data-ttu-id="1a2ec-114">Compilar o código do sombreador</span><span class="sxs-lookup"><span data-stu-id="1a2ec-114">Compile your shader code</span></span>
-   <span data-ttu-id="1a2ec-115">Carregar o código compilado em uma biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="1a2ec-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="1a2ec-116">Associar os recursos dos slots de origem aos slots de destino</span><span class="sxs-lookup"><span data-stu-id="1a2ec-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="1a2ec-117">Construir FLGs (função-vinculação-grafos) para sombreadores</span><span class="sxs-lookup"><span data-stu-id="1a2ec-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="1a2ec-118">Vincular grafos de sombreador com uma biblioteca de sombreador para produzir um blob de sombreador que o tempo de execução do Direct3D pode usar</span><span class="sxs-lookup"><span data-stu-id="1a2ec-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="1a2ec-119">Em seguida, criamos uma biblioteca de sombreador e ligamos os recursos dos slots de origem aos slots de destino.</span><span class="sxs-lookup"><span data-stu-id="1a2ec-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="1a2ec-120">Empacotando uma biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="1a2ec-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="1a2ec-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a2ec-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a2ec-122">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="1a2ec-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="1a2ec-123">Elementos gráficos do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1a2ec-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="1a2ec-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="1a2ec-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 