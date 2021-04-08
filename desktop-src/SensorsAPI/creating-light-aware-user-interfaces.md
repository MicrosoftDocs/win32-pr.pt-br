---
description: Esta seção aborda o uso de dados do sensor de luz ambiente e como os recursos da interface do usuário e o conteúdo do programa podem ser otimizados para muitas condições de iluminação.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Criando Light-Aware interfaces de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922234"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="c5f9f-103">Criando Light-Aware interfaces de usuário</span><span class="sxs-lookup"><span data-stu-id="c5f9f-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="c5f9f-104">Esta seção aborda o uso de dados do sensor de luz ambiente e como os recursos da interface do usuário e o conteúdo do programa podem ser otimizados para muitas condições de iluminação.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="c5f9f-105">Sensores de luz ambiente expõem dados que podem ser usados para determinar vários aspectos das condições de iluminação em que o sensor está localizado.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="c5f9f-106">Os sensores de luz ambiente podem expor o brilho geral de um ambiente (illuminance) e outros aspectos da luz ao redor, como a luminosidade ou a temperatura de cor.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="c5f9f-107">Os computadores podem ser mais úteis de várias maneiras quando o sistema está respondendo às condições de iluminação.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="c5f9f-108">Isso inclui controlar o brilho da tela do computador (um novo recurso totalmente suportado no Windows 7), ajustando automaticamente o nível de iluminação de teclados acesos e até mesmo o controle de brilho para outras luzes (como iluminação de botão, luzes de atividade e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c5f9f-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="c5f9f-109">Os programas do usuário final também podem se beneficiar de sensores leves.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="c5f9f-110">Os programas podem aplicar um tema apropriado para uma condição de iluminação específica, como um tema externo específico e um tema interno.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="c5f9f-111">Talvez o aspecto mais importante da integração do sensor leve com os programas seja a legibilidade e as otimizações legíveis baseadas em condições de iluminação.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="c5f9f-112">A API do sensor permite que você crie esses programas.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="c5f9f-113">Considere este cenário.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="c5f9f-114">Cenário: usando seu laptop para navegar até um restaurante</span><span class="sxs-lookup"><span data-stu-id="c5f9f-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="c5f9f-115">Suponha que você deseja usar seu computador para ajudá-lo a navegar para um novo restaurante.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="c5f9f-116">Você começa em sua casa, pesquisando o endereço do restaurante e planejando sua rota.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="c5f9f-117">A captura de tela a seguir mostra como o programa de navegação pode otimizar sua interface do usuário para mostrar informações detalhadas em condições de iluminação interna.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![interface do usuário projetada para iluminação em inglês.](images/nav-normal.png)

<span data-ttu-id="c5f9f-119">Quando você vai para o carro, encontra a luz solar direta, o que torna a tela do laptop difícil de ler.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="c5f9f-120">A captura de tela a seguir mostra como o seu programa pode alterar sua interface do usuário para maximizar a legibilidade/legibilidade na luz direta.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="c5f9f-121">Nessa exibição, muitos dos detalhes foram omitidos e o contraste é maximizado.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![interface do usuário projetada para condições de iluminação direta.](images/nav-contrast.png)

<span data-ttu-id="c5f9f-123">À medida que você se aproximar do restaurante, as abordagens da noite e ficam escuras para fora.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="c5f9f-124">Na captura de tela a seguir, a interface do usuário do programa de navegação foi otimizada para exibição de baixa luz.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="c5f9f-125">Usando cores mais escuras no geral, essa interface do usuário é fácil de resumir no carro escuro.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![interface do usuário projetada para exibição de baixa luz.](images/nav-lowlight.png)

<span data-ttu-id="c5f9f-127">No restante desta seção, você irá explorar algumas coisas que pode fazer para otimizar seus programas para várias condições de iluminação e como você pode usar a API do sensor para ajudar a habilitar a interface do usuário com reconhecimento claro.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5f9f-128">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c5f9f-128">In This Section</span></span>

-   [<span data-ttu-id="c5f9f-129">Conceitos básicos de Light-Aware interfaces de usuário</span><span class="sxs-lookup"><span data-stu-id="c5f9f-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="c5f9f-130">Exemplos de interfaces de usuário do Light-Aware</span><span class="sxs-lookup"><span data-stu-id="c5f9f-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="c5f9f-131">Otimizando a experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="c5f9f-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="c5f9f-132">Compreendendo e interpretando valores de Lux</span><span class="sxs-lookup"><span data-stu-id="c5f9f-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="c5f9f-133">Usando dados de sensor claro</span><span class="sxs-lookup"><span data-stu-id="c5f9f-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



