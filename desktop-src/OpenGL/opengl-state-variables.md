---
title: Variáveis de estado OpenGL
description: Os tópicos a seguir listam os nomes das variáveis de estado que podem ser consultadas
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variáveis de estado OpenGL
- variáveis de estado, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753730"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="e405f-105">Variáveis de estado OpenGL</span><span class="sxs-lookup"><span data-stu-id="e405f-105">OpenGL State Variables</span></span>

<span data-ttu-id="e405f-106">Os tópicos a seguir listam os nomes das variáveis de estado que podem ser consultadas:</span><span class="sxs-lookup"><span data-stu-id="e405f-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="e405f-107">**Variáveis de estado para valores atuais e dados associados**</span><span class="sxs-lookup"><span data-stu-id="e405f-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="e405f-108">**Variáveis de estado de transformação**</span><span class="sxs-lookup"><span data-stu-id="e405f-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="e405f-109">**Variáveis de estado de coloração**</span><span class="sxs-lookup"><span data-stu-id="e405f-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="e405f-110">**Variáveis de estado de iluminação**</span><span class="sxs-lookup"><span data-stu-id="e405f-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="e405f-111">**Variáveis de estado de rasterização**</span><span class="sxs-lookup"><span data-stu-id="e405f-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="e405f-112">**Variáveis de estado texturing**</span><span class="sxs-lookup"><span data-stu-id="e405f-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="e405f-113">**Operações de pixel**</span><span class="sxs-lookup"><span data-stu-id="e405f-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="e405f-114">**Variáveis de estado de controle framebuffer**</span><span class="sxs-lookup"><span data-stu-id="e405f-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="e405f-115">**Variáveis de estado de pixel**</span><span class="sxs-lookup"><span data-stu-id="e405f-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="e405f-116">**Variáveis de estado do avaliador**</span><span class="sxs-lookup"><span data-stu-id="e405f-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="e405f-117">**Variáveis de estado de dica**</span><span class="sxs-lookup"><span data-stu-id="e405f-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="e405f-118">**Variáveis de estado dependentes da implementação**</span><span class="sxs-lookup"><span data-stu-id="e405f-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="e405f-119">**Variáveis de estado de Pixel-Depth dependentes da implementação**</span><span class="sxs-lookup"><span data-stu-id="e405f-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="e405f-120">**Variáveis de estado diversas**</span><span class="sxs-lookup"><span data-stu-id="e405f-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="e405f-121">Para cada variável, o tópico lista uma descrição, um grupo de atributos, um valor inicial ou mínimo e a função [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) sugerida a ser usada para obtê-lo.</span><span class="sxs-lookup"><span data-stu-id="e405f-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="e405f-122">As variáveis de estado que você pode obter usando [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetDoublev**](glgetdoublev.md) são listadas com apenas um desses functionsthe, que é mais apropriado para o tipo de dados a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="e405f-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="e405f-123">Você não pode obter essas variáveis de estado usando [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="e405f-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="e405f-124">No entanto, você pode obter variáveis de estado para as quais **glIsEnabled** está listado como a função de consulta com **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** e **glGetDoublev**.</span><span class="sxs-lookup"><span data-stu-id="e405f-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="e405f-125">Você pode obter variáveis de estado para as quais qualquer outra função está listada como a função de consulta somente usando essa função.</span><span class="sxs-lookup"><span data-stu-id="e405f-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="e405f-126">Se nenhum grupo de atributos estiver listado, a variável não pertence a nenhum grupo.</span><span class="sxs-lookup"><span data-stu-id="e405f-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="e405f-127">Todas as variáveis de estado que você pode consultar, exceto aquelas que são dependentes de implementação, têm valores iniciais.</span><span class="sxs-lookup"><span data-stu-id="e405f-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="e405f-128">Para determinar o valor inicial de uma variável para a qual nenhum valor inicial está listado, consulte a referência da variável ou a</span><span class="sxs-lookup"><span data-stu-id="e405f-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="e405f-129">*Manual de referência OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="e405f-129">*OpenGL Reference Manual*.</span></span>

 

 




