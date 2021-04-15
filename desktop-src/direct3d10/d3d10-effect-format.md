---
description: Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370501"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="eb33e-103">Formato de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="eb33e-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="eb33e-104">Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito.</span><span class="sxs-lookup"><span data-stu-id="eb33e-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="eb33e-105">O estado do efeito pode ser basicamente dividido em três categorias:</span><span class="sxs-lookup"><span data-stu-id="eb33e-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="eb33e-106">[Variáveis](d3d10-effect-variable-syntax.md), que geralmente são declaradas na parte superior de um efeito.</span><span class="sxs-lookup"><span data-stu-id="eb33e-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="eb33e-107">[Funções](d3d10-effect-function-syntax.md), que implementam o código de sombreador ou são usadas como funções auxiliares por outras funções.</span><span class="sxs-lookup"><span data-stu-id="eb33e-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="eb33e-108">[Uma técnica](d3d10-effect-technique-syntax.md), que implementa sequências de renderização usando um ou mais efeitos aprovados.</span><span class="sxs-lookup"><span data-stu-id="eb33e-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="eb33e-109">Cada passagem define um ou mais [grupos de Estados](d3d10-effect-states.md) e chama funções de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eb33e-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![diagrama das categorias de estado de efeito](images/d3d10-effect-intro.png)

<span data-ttu-id="eb33e-111">O diagrama anterior mostra as categorias de estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="eb33e-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb33e-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb33e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb33e-113">Referência de efeito</span><span class="sxs-lookup"><span data-stu-id="eb33e-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



