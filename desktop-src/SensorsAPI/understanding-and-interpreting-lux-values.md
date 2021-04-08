---
description: O tipo de dados principal do sensor para sensores de luz ambiente é illuminance em Lux (lumens por metro quadrado). Os princípios descritos neste tópico se baseiam na obtenção de valores de Lux como entrada e na reação a esses dados em um programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Compreendendo e interpretando valores de Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011358"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="f573e-104">Compreendendo e interpretando valores de Lux</span><span class="sxs-lookup"><span data-stu-id="f573e-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="f573e-105">O tipo de dados principal do sensor para sensores de luz ambiente é illuminance em Lux (lumens por metro quadrado).</span><span class="sxs-lookup"><span data-stu-id="f573e-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="f573e-106">Os princípios descritos neste tópico se baseiam na obtenção de valores de Lux como entrada e na reação a esses dados em um programa.</span><span class="sxs-lookup"><span data-stu-id="f573e-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="f573e-107">As leituras de Lux são diretamente proporcionais à energia por medidor quadrado absorvido por segundo.</span><span class="sxs-lookup"><span data-stu-id="f573e-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="f573e-108">A percepção humana dos níveis de luz não é tão simples.</span><span class="sxs-lookup"><span data-stu-id="f573e-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="f573e-109">A percepção humana da luz é complicada porque nossos olhos estão constantemente ajustando e outros processos biológicos estão afetando nossa percepção.</span><span class="sxs-lookup"><span data-stu-id="f573e-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="f573e-110">No entanto, podemos imaginar essa percepção de uma perspectiva simplificada criando vários intervalos de interesse com limites superiores e inferiores conhecidos.</span><span class="sxs-lookup"><span data-stu-id="f573e-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="f573e-111">O conjunto de dados de exemplo a seguir representa limites aproximados para condições de iluminação comuns e a etapa de iluminação correspondente.</span><span class="sxs-lookup"><span data-stu-id="f573e-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="f573e-112">Aqui, cada etapa de iluminação representa uma alteração no ambiente de iluminação.</span><span class="sxs-lookup"><span data-stu-id="f573e-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="f573e-113">Esse conjunto de dados é para ilustração e pode não ser completamente preciso para todos os usuários ou situações.</span><span class="sxs-lookup"><span data-stu-id="f573e-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="f573e-114">Condição de iluminação</span><span class="sxs-lookup"><span data-stu-id="f573e-114">Lighting condition</span></span> | <span data-ttu-id="f573e-115">De (Lux)</span><span class="sxs-lookup"><span data-stu-id="f573e-115">From (lux)</span></span> | <span data-ttu-id="f573e-116">Para (Lux)</span><span class="sxs-lookup"><span data-stu-id="f573e-116">To (lux)</span></span> | <span data-ttu-id="f573e-117">Valor médio (Lux)</span><span class="sxs-lookup"><span data-stu-id="f573e-117">Mean value (lux)</span></span> | <span data-ttu-id="f573e-118">Etapa de iluminação</span><span class="sxs-lookup"><span data-stu-id="f573e-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="f573e-119">Preto-Tom</span><span class="sxs-lookup"><span data-stu-id="f573e-119">Pitch Black</span></span>        | <span data-ttu-id="f573e-120">0</span><span class="sxs-lookup"><span data-stu-id="f573e-120">0</span></span>          | <span data-ttu-id="f573e-121">10</span><span class="sxs-lookup"><span data-stu-id="f573e-121">10</span></span>       | <span data-ttu-id="f573e-122">5</span><span class="sxs-lookup"><span data-stu-id="f573e-122">5</span></span>                | <span data-ttu-id="f573e-123">1</span><span class="sxs-lookup"><span data-stu-id="f573e-123">1</span></span>             |
| <span data-ttu-id="f573e-124">Muito escuro</span><span class="sxs-lookup"><span data-stu-id="f573e-124">Very Dark</span></span>          | <span data-ttu-id="f573e-125">11</span><span class="sxs-lookup"><span data-stu-id="f573e-125">11</span></span>         | <span data-ttu-id="f573e-126">50</span><span class="sxs-lookup"><span data-stu-id="f573e-126">50</span></span>       | <span data-ttu-id="f573e-127">30</span><span class="sxs-lookup"><span data-stu-id="f573e-127">30</span></span>               | <span data-ttu-id="f573e-128">2</span><span class="sxs-lookup"><span data-stu-id="f573e-128">2</span></span>             |
| <span data-ttu-id="f573e-129">Inportais escuras</span><span class="sxs-lookup"><span data-stu-id="f573e-129">Dark Indoors</span></span>       | <span data-ttu-id="f573e-130">51</span><span class="sxs-lookup"><span data-stu-id="f573e-130">51</span></span>         | <span data-ttu-id="f573e-131">200</span><span class="sxs-lookup"><span data-stu-id="f573e-131">200</span></span>      | <span data-ttu-id="f573e-132">125</span><span class="sxs-lookup"><span data-stu-id="f573e-132">125</span></span>              | <span data-ttu-id="f573e-133">3</span><span class="sxs-lookup"><span data-stu-id="f573e-133">3</span></span>             |
| <span data-ttu-id="f573e-134">Dim inportations</span><span class="sxs-lookup"><span data-stu-id="f573e-134">Dim Indoors</span></span>        | <span data-ttu-id="f573e-135">201</span><span class="sxs-lookup"><span data-stu-id="f573e-135">201</span></span>        | <span data-ttu-id="f573e-136">400</span><span class="sxs-lookup"><span data-stu-id="f573e-136">400</span></span>      | <span data-ttu-id="f573e-137">300</span><span class="sxs-lookup"><span data-stu-id="f573e-137">300</span></span>              | <span data-ttu-id="f573e-138">4</span><span class="sxs-lookup"><span data-stu-id="f573e-138">4</span></span>             |
| <span data-ttu-id="f573e-139">Inportações normais</span><span class="sxs-lookup"><span data-stu-id="f573e-139">Normal Indoors</span></span>     | <span data-ttu-id="f573e-140">401</span><span class="sxs-lookup"><span data-stu-id="f573e-140">401</span></span>        | <span data-ttu-id="f573e-141">1000</span><span class="sxs-lookup"><span data-stu-id="f573e-141">1000</span></span>     | <span data-ttu-id="f573e-142">700</span><span class="sxs-lookup"><span data-stu-id="f573e-142">700</span></span>              | <span data-ttu-id="f573e-143">5</span><span class="sxs-lookup"><span data-stu-id="f573e-143">5</span></span>             |
| <span data-ttu-id="f573e-144">Inportações brilhantes</span><span class="sxs-lookup"><span data-stu-id="f573e-144">Bright Indoors</span></span>     | <span data-ttu-id="f573e-145">1001</span><span class="sxs-lookup"><span data-stu-id="f573e-145">1001</span></span>       | <span data-ttu-id="f573e-146">5.000</span><span class="sxs-lookup"><span data-stu-id="f573e-146">5000</span></span>     | <span data-ttu-id="f573e-147">3000</span><span class="sxs-lookup"><span data-stu-id="f573e-147">3000</span></span>             | <span data-ttu-id="f573e-148">6</span><span class="sxs-lookup"><span data-stu-id="f573e-148">6</span></span>             |
| <span data-ttu-id="f573e-149">Dim livre</span><span class="sxs-lookup"><span data-stu-id="f573e-149">Dim Outdoors</span></span>       | <span data-ttu-id="f573e-150">5001</span><span class="sxs-lookup"><span data-stu-id="f573e-150">5001</span></span>       | <span data-ttu-id="f573e-151">10.000</span><span class="sxs-lookup"><span data-stu-id="f573e-151">10,000</span></span>   | <span data-ttu-id="f573e-152">7500</span><span class="sxs-lookup"><span data-stu-id="f573e-152">7500</span></span>             | <span data-ttu-id="f573e-153">7</span><span class="sxs-lookup"><span data-stu-id="f573e-153">7</span></span>             |
| <span data-ttu-id="f573e-154">Em nuvem em casa</span><span class="sxs-lookup"><span data-stu-id="f573e-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="f573e-155">10.001</span><span class="sxs-lookup"><span data-stu-id="f573e-155">10,001</span></span>     | <span data-ttu-id="f573e-156">30,000</span><span class="sxs-lookup"><span data-stu-id="f573e-156">30,000</span></span>   | <span data-ttu-id="f573e-157">20.000</span><span class="sxs-lookup"><span data-stu-id="f573e-157">20,000</span></span>           | <span data-ttu-id="f573e-158">8</span><span class="sxs-lookup"><span data-stu-id="f573e-158">8</span></span>             |
| <span data-ttu-id="f573e-159">Luz solar direta</span><span class="sxs-lookup"><span data-stu-id="f573e-159">Direct Sunlight</span></span>    | <span data-ttu-id="f573e-160">30.001</span><span class="sxs-lookup"><span data-stu-id="f573e-160">30,001</span></span>     | <span data-ttu-id="f573e-161">100.000</span><span class="sxs-lookup"><span data-stu-id="f573e-161">100,000</span></span>  | <span data-ttu-id="f573e-162">65.000</span><span class="sxs-lookup"><span data-stu-id="f573e-162">65,000</span></span>           | <span data-ttu-id="f573e-163">9</span><span class="sxs-lookup"><span data-stu-id="f573e-163">9</span></span>             |



 

<span data-ttu-id="f573e-164">Se visualizarmos esses dados usando os valores médios desta tabela, veremos que a relação Lux-to-Light-Step não é linear, como mostrado no grafo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f573e-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![grafo illuminance linear](images/luxtostep.png)

<span data-ttu-id="f573e-166">No entanto, se exibirmos esses dados usando uma escala logarítmica no eixo x, podemos ver que uma relação aproximadamente linear surge.</span><span class="sxs-lookup"><span data-stu-id="f573e-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![grafo illuminance logarítmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="f573e-168">Um exemplo de transformação</span><span class="sxs-lookup"><span data-stu-id="f573e-168">An Example Transform</span></span>

<span data-ttu-id="f573e-169">Com base no conjunto de dados de exemplo para sensores de luz ambiente fornecidos anteriormente, você pode chegar à equação a seguir para mapear valores de Lux para a percepção humana.</span><span class="sxs-lookup"><span data-stu-id="f573e-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="f573e-170">Neste exemplo, os valores esperados variam de 0 Lux a 1 milhão Lux.</span><span class="sxs-lookup"><span data-stu-id="f573e-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![equação de valor de Lux](images/sensor-lux-equation.jpg)

<span data-ttu-id="f573e-172">Esta equação resulta em valores que variam de maneira ligeiramente linear entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="f573e-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="f573e-173">Esse resultado indica como a iluminação percebida pelo homem foi alterada com base no conjunto de dados de exemplo mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f573e-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



