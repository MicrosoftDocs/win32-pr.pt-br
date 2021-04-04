---
title: Usando as funções de configuração do monitor de Low-Level
description: Usando as funções de configuração do monitor de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitorar, funções
- monitorar, funções de configuração de nível baixo
- monitor, DDC/CI
- monitorar, exibir a interface de comando do canal de dados
- configurações do monitor, funções de configuração de nível baixo
- configuração do monitor, funções
- configuração do monitor, DDC/CI
- configuração do monitor, exibição da interface de comando do canal de dados
- funções de configuração de nível baixo
- Exibir interface de comando de canal de dados
- DDC/CI
- Conjunto de comandos de controle de monitor VESA (MCCS)
- Conjunto de comandos de controle de monitor (MCCS)
- MCCS (conjunto de comandos de controle de monitor)
- Painel de controle virtual (VCP)
- VCP (painel de controle virtual)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917248"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="fd253-119">Usando as funções de configuração do monitor de Low-Level</span><span class="sxs-lookup"><span data-stu-id="fd253-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="fd253-120">Antes de usar as funções de configuração de monitor de nível baixo, você deve estar familiarizado com estes padrões:</span><span class="sxs-lookup"><span data-stu-id="fd253-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="fd253-121">Exibir a interface de comando do canal de dados (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="fd253-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="fd253-122">Conjunto de comandos de controle de monitor VESA (MCCS)</span><span class="sxs-lookup"><span data-stu-id="fd253-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="fd253-123">As funções de nível baixo funcionam obtendo e definindo os valores dos códigos do painel de controle virtual (VCP).</span><span class="sxs-lookup"><span data-stu-id="fd253-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="fd253-124">Um código VCP pode ser *contínuo* ou não *contínuo*.</span><span class="sxs-lookup"><span data-stu-id="fd253-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="fd253-125">Os códigos contínuos podem assumir qualquer valor entre zero e um valor máximo específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fd253-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="fd253-126">Códigos não contínuos dão suporte a um conjunto definido de valores, que também são específicos para o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="fd253-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="fd253-127">Para usar as funções de configuração do monitor de baixo nível, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fd253-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="fd253-128">Obtenha um identificador de **HMONITOR** chamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) ou [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span><span class="sxs-lookup"><span data-stu-id="fd253-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="fd253-129">Chame [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) para obter o número de monitores físicos associados ao identificador **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="fd253-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="fd253-130">Chame [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) para obter uma lista de identificadores para os monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="fd253-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="fd253-131">Chame [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) para obter o comprimento da cadeia de caracteres de recursos DDC/CI de um monitor.</span><span class="sxs-lookup"><span data-stu-id="fd253-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="fd253-132">A cadeia de caracteres de funcionalidades é uma cadeia de caracteres ASCII que contém informações estáticas sobre o monitor.</span><span class="sxs-lookup"><span data-stu-id="fd253-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="fd253-133">Uma parte da cadeia de caracteres lista os códigos de VCP aos quais o monitor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="fd253-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="fd253-134">A cadeia de caracteres também lista os valores com suporte dos códigos VCP não contínuos.</span><span class="sxs-lookup"><span data-stu-id="fd253-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="fd253-135">Aloque um buffer para manter a cadeia de caracteres de recursos e chame [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) para obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fd253-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="fd253-136">Analise a cadeia de caracteres de funcionalidades para determinar quais códigos de VCP são compatíveis com o monitor.</span><span class="sxs-lookup"><span data-stu-id="fd253-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="fd253-137">Para um código VCP contínuo, chame [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) para obter os valores atuais e máximos do código.</span><span class="sxs-lookup"><span data-stu-id="fd253-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="fd253-138">Para um código VCP não contínuo, analise a cadeia de caracteres de funcionalidades para obter os valores com suporte.</span><span class="sxs-lookup"><span data-stu-id="fd253-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="fd253-139">Chame [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) para definir um novo valor para um código VCP.</span><span class="sxs-lookup"><span data-stu-id="fd253-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd253-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd253-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd253-141">**Usando a configuração do monitor**</span><span class="sxs-lookup"><span data-stu-id="fd253-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 