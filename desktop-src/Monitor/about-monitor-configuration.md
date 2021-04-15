---
title: Sobre a configuração do monitor
description: Sobre a configuração do monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitorar, sobre
- monitor, calibração de cor
- monitor, ajuste da área de exibição do monitor
- monitorar, salvar configurações do monitor
- monitorar, restaurar configurações do monitor
- monitorar, recursos do fornecedor
- calibragem de cores
- ajustando a área de exibição do monitor
- Salvando configurações do monitor
- Restaurando configurações do monitor
- recursos do fornecedor
- configuração do monitor, calibragem de cores
- monitorar a configuração, sobre
- configuração do monitor, ajuste da área de exibição do monitor
- configuração do monitor, salvando configurações do monitor
- configuração do monitor, Restaurando configurações do monitor
- configuração do monitor, recursos do fornecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498675"
---
# <a name="about-monitor-configuration"></a><span data-ttu-id="d69c8-120">Sobre a configuração do monitor</span><span class="sxs-lookup"><span data-stu-id="d69c8-120">About Monitor Configuration</span></span>

<span data-ttu-id="d69c8-121">Os usos para as funções de configuração do monitor incluem:</span><span class="sxs-lookup"><span data-stu-id="d69c8-121">Uses for the monitor configuration functions include:</span></span>

-   <span data-ttu-id="d69c8-122">Calibragem de cor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-122">Color calibration.</span></span> <span data-ttu-id="d69c8-123">Um monitor calibrado corretamente reproduz cores corretamente.</span><span class="sxs-lookup"><span data-stu-id="d69c8-123">A properly calibrated monitor reproduces colors correctly.</span></span> <span data-ttu-id="d69c8-124">Normalmente, um aplicativo de calibragem de cor exibe um padrão de teste e tem controles para alterar uma configuração de monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-124">Typically, a color calibration application displays a test pattern and has controls to change a monitor setting.</span></span> <span data-ttu-id="d69c8-125">O usuário altera a configuração até que uma condição seja atendida e repete esse processo para cada configuração de monitor até que o monitor seja calibrado.</span><span class="sxs-lookup"><span data-stu-id="d69c8-125">The user changes the setting until a condition is met, and repeats this process for each monitor setting until the monitor is calibrated.</span></span>
-   <span data-ttu-id="d69c8-126">Ajustando a área de exibição do monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-126">Adjusting the monitor's display area.</span></span> <span data-ttu-id="d69c8-127">As funções de configuração do monitor podem ser usadas para alterar o tamanho e a posição da área de exibição de um monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-127">The monitor configuration functions can be used to change the size and position of a monitor's display area.</span></span> <span data-ttu-id="d69c8-128">Por exemplo, quando um monitor de LCD está conectado a um computador usando um conector analógico, a melhor qualidade de imagem é obtida quando há um mapeamento de um para um entre pixels no buffer de quadro da placa gráfica e pixels no monitor LCD.</span><span class="sxs-lookup"><span data-stu-id="d69c8-128">For example, when an LCD monitor is connected to a computer by using an analog connector, the best image quality is obtained when there is a one-to-one mapping between pixels in the graphics card's frame buffer and pixels on the LCD monitor.</span></span>
-   <span data-ttu-id="d69c8-129">Salvando e restaurando configurações do monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-129">Saving and restoring monitor settings.</span></span> <span data-ttu-id="d69c8-130">Alguns usuários precisam de vários conjuntos de configurações de monitor, pois diferentes cenários exigem configurações de monitor diferentes.</span><span class="sxs-lookup"><span data-stu-id="d69c8-130">Some users need multiple sets of monitor settings, because different scenarios require different monitor settings.</span></span> <span data-ttu-id="d69c8-131">Por exemplo, as configurações de monitor ideais para aplicativos de área de trabalho não são ideais para assistir à televisão.</span><span class="sxs-lookup"><span data-stu-id="d69c8-131">For example, monitor settings that are optimal for desktop applications are not optimal for watching television.</span></span>
-   <span data-ttu-id="d69c8-132">Usando recursos de monitor específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-132">Using vendor-specific monitor features.</span></span> <span data-ttu-id="d69c8-133">Usando as funções de configuração do monitor, os fabricantes podem criar aplicativos que usam os recursos específicos do fornecedor do monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-133">Using the monitor configuration functions, manufacturers can create applications that use the vendor-specific features of the monitor.</span></span>

<span data-ttu-id="d69c8-134">As funções de configuração do monitor são divididas em funções de alto nível e de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="d69c8-134">The monitor configuration functions are divided into high-level and low-level functions.</span></span> <span data-ttu-id="d69c8-135">As funções de alto nível são mais fáceis de usar do que as funções de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d69c8-135">The high-level functions are easier to use than the low-level functions.</span></span> <span data-ttu-id="d69c8-136">Para usar as funções de alto nível, você não precisa saber nada sobre a interface de comando de canal de dados de exibição (DDC/CI).</span><span class="sxs-lookup"><span data-stu-id="d69c8-136">To use the high-level functions, you do not need to know anything about the Display Data Channel Command Interface (DDC/CI).</span></span> <span data-ttu-id="d69c8-137">No entanto, as funções de alto nível não oferecem acesso a recursos específicos do fornecedor do monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-137">However, the high-level functions do not give you access to vendor-specific features of the monitor.</span></span>

<span data-ttu-id="d69c8-138">As funções de nível baixo são um wrapper fino em volta dos comandos DDC/CI.</span><span class="sxs-lookup"><span data-stu-id="d69c8-138">The low-level functions are a thin wrapper around the DDC/CI commands.</span></span> <span data-ttu-id="d69c8-139">Para usar as funções de nível inferior, você deve estar familiarizado com o padrão DDC/CI e também com o padrão MCCS (VESA monitor Control Set).</span><span class="sxs-lookup"><span data-stu-id="d69c8-139">To use the low-level functions, you must be familiar with the DDC/CI standard and also with the VESA Monitor Control Command Set (MCCS) standard.</span></span> <span data-ttu-id="d69c8-140">Em geral, você deve usar as funções de alto nível, a menos que precise usar recursos que estão disponíveis apenas nas funções de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="d69c8-140">Generally, you should use the high-level functions unless you need to use features that are available only in the low-level functions.</span></span>

<span data-ttu-id="d69c8-141">As funções de configuração de monitor de alto nível são projetadas para que um aplicativo não possa colocar um monitor em um estado inutilizável.</span><span class="sxs-lookup"><span data-stu-id="d69c8-141">The high-level monitor configuration functions are designed so that an application cannot put a monitor into an unusable state.</span></span> <span data-ttu-id="d69c8-142">As funções de nível baixo podem ser usadas para enviar códigos VCP ao monitor.</span><span class="sxs-lookup"><span data-stu-id="d69c8-142">The low-level functions can be used to send VCP codes to the monitor.</span></span> <span data-ttu-id="d69c8-143">No entanto, lembre-se de que alguns códigos de VCP podem desabilitar a funcionalidade importante ou colocar o monitor em um estado em que o usuário não consegue ver a imagem de exibição.</span><span class="sxs-lookup"><span data-stu-id="d69c8-143">However, be aware that some VCP codes can disable important functionality or put the monitor into a state where the user cannot see the display image.</span></span> <span data-ttu-id="d69c8-144">Para obter mais informações, consulte o padrão do conjunto de comandos do controle de monitor VESA (MCCS).</span><span class="sxs-lookup"><span data-stu-id="d69c8-144">For more information, see the VESA Monitor Control Command Set (MCCS) standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d69c8-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d69c8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d69c8-146">Configuração do monitor</span><span class="sxs-lookup"><span data-stu-id="d69c8-146">Monitor Configuration</span></span>](monitor-configuration.md)
</dt> </dl>

 

 




