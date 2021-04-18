---
description: GUIDs de configuração de energia identificam eventos de alteração de energia.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUIDs de configuração de energia (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810288"
---
# <a name="power-setting-guids"></a><span data-ttu-id="78357-103">GUIDs de configuração de energia</span><span class="sxs-lookup"><span data-stu-id="78357-103">Power Setting GUIDs</span></span>

<span data-ttu-id="78357-104">A configuração de energia **GUID** s identifica eventos de alteração de energia.</span><span class="sxs-lookup"><span data-stu-id="78357-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="78357-105">Este tópico lista as configurações de energia **GUID** s para notificações que são mais úteis para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="78357-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="78357-106">Um aplicativo deve se registrar para cada evento de alteração de energia que possa afetar seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="78357-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="78357-107">A notificação é enviada cada vez que uma configuração é alterada.</span><span class="sxs-lookup"><span data-stu-id="78357-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="78357-108">As configurações de energia **GUID** s são definidas em Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="78357-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="78357-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**fonte de energia do GUID \_ ACDC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="78357-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="78357-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="78357-111">A fonte de energia do sistema foi alterada.</span><span class="sxs-lookup"><span data-stu-id="78357-111">The system power source has changed.</span></span> <span data-ttu-id="78357-112">O membro de **dados** é um **DWORD** com valores da enumeração de [**\_ \_ condição de energia do sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) que indica a fonte de energia atual.</span><span class="sxs-lookup"><span data-stu-id="78357-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="78357-113">**PoAc** (0)-o computador é alimentado por uma fonte de energia CA (ou semelhante, como um laptop alimentado por um adaptador automotivo de 12V).</span><span class="sxs-lookup"><span data-stu-id="78357-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="78357-114">**PoDc** (1)-o computador é alimentado por uma fonte de energia de bateria integrada.</span><span class="sxs-lookup"><span data-stu-id="78357-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="78357-115">**PoHot** (2)-o computador é alimentado por uma fonte de energia de curto prazo, como um dispositivo UPS.</span><span class="sxs-lookup"><span data-stu-id="78357-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="78357-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**porcentagem de bateria de GUID \_ \_ \_ restante**</span><span class="sxs-lookup"><span data-stu-id="78357-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="78357-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="78357-118">A capacidade restante da bateria foi alterada.</span><span class="sxs-lookup"><span data-stu-id="78357-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="78357-119">A granularidade varia de sistema para sistema, mas a granularidade mais fina é 1%.</span><span class="sxs-lookup"><span data-stu-id="78357-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="78357-120">O membro de **dados** é um **DWORD** que indica a capacidade da bateria atual restante como uma porcentagem de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="78357-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78357-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_estado de \_ exibição do console GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="78357-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="78357-123">O estado de exibição do monitor atual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="78357-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="78357-124">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa notificação está disponível a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="78357-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="78357-125">O membro de **dados** é um **DWORD** com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="78357-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="78357-126">0x0-a exibição está desativada.</span><span class="sxs-lookup"><span data-stu-id="78357-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="78357-127">0x1-a exibição está ativada.</span><span class="sxs-lookup"><span data-stu-id="78357-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="78357-128">0x2-a exibição está esmaecida.</span><span class="sxs-lookup"><span data-stu-id="78357-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="78357-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_presença do \_ usuário \_ global do GUID**</span><span class="sxs-lookup"><span data-stu-id="78357-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="78357-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="78357-131">O status do usuário associado a qualquer sessão foi alterado.</span><span class="sxs-lookup"><span data-stu-id="78357-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="78357-132">Isso representa o status combinado da presença do usuário em todas as sessões locais e remotas no sistema.</span><span class="sxs-lookup"><span data-stu-id="78357-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="78357-133">Essa notificação é enviada somente para serviços e outros programas em execução na sessão 0.</span><span class="sxs-lookup"><span data-stu-id="78357-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="78357-134">Os aplicativos de modo de usuário devem se registrar para a **\_ presença de \_ usuário \_ de sessão GUID** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="78357-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="78357-135">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa notificação está disponível a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="78357-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="78357-136">O membro de **dados** é um **DWORD** com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="78357-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="78357-137">**PowerUserPresent** (0)-o usuário está presente em qualquer sessão local ou remota no sistema.</span><span class="sxs-lookup"><span data-stu-id="78357-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="78357-138">**PowerUserInactive** (2)-o usuário não está presente em nenhuma sessão local ou remota no sistema.</span><span class="sxs-lookup"><span data-stu-id="78357-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="78357-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_tarefa de \_ segundo plano de ociosidade do GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="78357-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="78357-141">O sistema está ocupado.</span><span class="sxs-lookup"><span data-stu-id="78357-141">The system is busy.</span></span> <span data-ttu-id="78357-142">Isso indica que o sistema não estará mudando para um estado ocioso em um futuro próximo e que a hora atual é um bom momento para que os componentes executem tarefas de segundo plano ou ociosas que, de outra forma, impediriam que o computador entrasse em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="78357-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="78357-143">Não há nenhuma notificação quando o sistema é capaz de passar para um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="78357-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="78357-144">A notificação de tarefa de segundo plano ociosa não indica se um usuário está presente no computador.</span><span class="sxs-lookup"><span data-stu-id="78357-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="78357-145">O membro de **dados** não tem informações e pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="78357-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="78357-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ ativação do monitor \_ de GUID**</span><span class="sxs-lookup"><span data-stu-id="78357-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="78357-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="78357-148">O monitor do sistema primário foi ligado ou desligado.</span><span class="sxs-lookup"><span data-stu-id="78357-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="78357-149">Essa notificação é útil para componentes que processam ativamente o conteúdo para o dispositivo de vídeo, como a visualização de mídia.</span><span class="sxs-lookup"><span data-stu-id="78357-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="78357-150">Esses aplicativos devem se registrar para essa notificação e parar de renderizar o conteúdo de gráficos quando o monitor estiver desativado para reduzir o consumo de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="78357-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="78357-151">O membro de **dados** é um **DWORD** que indica o estado atual do monitor.</span><span class="sxs-lookup"><span data-stu-id="78357-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="78357-152">0x0-o monitor está desativado.</span><span class="sxs-lookup"><span data-stu-id="78357-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="78357-153">0x1-o monitor está ativado.</span><span class="sxs-lookup"><span data-stu-id="78357-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="78357-154">**Windows 8 e Windows Server 2012:** Os novos aplicativos devem usar o **\_ estado de \_ exibição \_ do console GUID** em vez desta notificação.</span><span class="sxs-lookup"><span data-stu-id="78357-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="78357-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_status de \_ economia de energia do GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="78357-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="78357-157">A economia de bateria foi desativada ou ativada em resposta à alteração das condições de energia.</span><span class="sxs-lookup"><span data-stu-id="78357-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="78357-158">Essa notificação é útil para os componentes que participam da conservação de energia.</span><span class="sxs-lookup"><span data-stu-id="78357-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="78357-159">Esses aplicativos devem se registrar para essa notificação e economizar energia quando a economia de bateria estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="78357-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="78357-160">O membro de **dados** é um **DWORD** que indica o estado de economia de bateria.</span><span class="sxs-lookup"><span data-stu-id="78357-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="78357-161">0x0-a economia de bateria está desativada.</span><span class="sxs-lookup"><span data-stu-id="78357-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="78357-162">0x1-a economia de bateria está ativada.</span><span class="sxs-lookup"><span data-stu-id="78357-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="78357-163">Economize energia sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="78357-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="78357-164">Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="78357-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="78357-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalidade POWERSCHEME do GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="78357-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="78357-167">A personalidade do esquema de energia ativo foi alterada.</span><span class="sxs-lookup"><span data-stu-id="78357-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="78357-168">Todos os esquemas de energia são mapeados para um desses personalidades.</span><span class="sxs-lookup"><span data-stu-id="78357-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="78357-169">O membro de **dados** é um **GUID** que indica a nova personalidade de esquema de energia ativo.</span><span class="sxs-lookup"><span data-stu-id="78357-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="78357-170">**GUID \_ do \_ \_ Economia mínima de energia** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span><span class="sxs-lookup"><span data-stu-id="78357-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="78357-171">Alto desempenho-o esquema foi projetado para oferecer o desempenho máximo às custas da economia de consumo de energia.</span><span class="sxs-lookup"><span data-stu-id="78357-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="78357-172">**GUID \_ do \_ \_ Economia máxima de energia** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="78357-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="78357-173">Economia de energia – o esquema foi projetado para oferecer economia de consumo de energia máxima às custas do desempenho e da capacidade de resposta do sistema.</span><span class="sxs-lookup"><span data-stu-id="78357-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="78357-174">**GUID \_ do \_ \_ Economia de energia típica** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span><span class="sxs-lookup"><span data-stu-id="78357-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="78357-175">Automático-o esquema foi projetado para balancear automaticamente o desempenho e a economia de consumo de energia.</span><span class="sxs-lookup"><span data-stu-id="78357-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="78357-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_status de \_ exibição da sessão GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="78357-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="78357-178">A exibição associada à sessão do aplicativo foi ligada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="78357-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="78357-179">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa notificação está disponível a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="78357-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="78357-180">Essa notificação é enviada somente para aplicativos de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="78357-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="78357-181">Os serviços e outros programas em execução na sessão 0 não recebem essa notificação.</span><span class="sxs-lookup"><span data-stu-id="78357-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="78357-182">O membro de **dados** é um **DWORD** com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="78357-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="78357-183">0x0-a exibição está desativada.</span><span class="sxs-lookup"><span data-stu-id="78357-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="78357-184">0x1-a exibição está ativada.</span><span class="sxs-lookup"><span data-stu-id="78357-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="78357-185">0x2-a exibição está esmaecida.</span><span class="sxs-lookup"><span data-stu-id="78357-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="78357-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_presença de \_ usuário de sessão GUID \_**</span><span class="sxs-lookup"><span data-stu-id="78357-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="78357-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="78357-188">O status do usuário associado à sessão do aplicativo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="78357-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="78357-189">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Essa notificação está disponível a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="78357-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="78357-190">Essa notificação é enviada somente para aplicativos de modo de usuário em execução em uma sessão interativa.</span><span class="sxs-lookup"><span data-stu-id="78357-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="78357-191">Os serviços e outros programas em execução na sessão 0 devem ser registrados para a **\_ \_ \_ presença do usuário global do GUID**.</span><span class="sxs-lookup"><span data-stu-id="78357-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="78357-192">O membro de **dados** é um **DWORD** com um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="78357-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="78357-193">**PowerUserPresent** (0)-o usuário está fornecendo entrada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="78357-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="78357-194">**PowerUserInactive** (2)-o tempo limite da atividade do usuário expirou sem interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="78357-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="78357-195">Todos os aplicativos executados em uma sessão de modo de usuário interativo devem usar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="78357-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="78357-196">Quando os aplicativos de modo kernel se registram para o status do monitor, eles devem usar o **\_ status de \_ exibição \_ do console GUID** .</span><span class="sxs-lookup"><span data-stu-id="78357-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="78357-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**sistema do GUID \_ \_ ausentemode**</span><span class="sxs-lookup"><span data-stu-id="78357-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78357-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="78357-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="78357-199">O sistema está entrando ou saindo do modo ausente.</span><span class="sxs-lookup"><span data-stu-id="78357-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="78357-200">O membro de **dados** é um **DWORD** que indica o estado atual do modo ausente.</span><span class="sxs-lookup"><span data-stu-id="78357-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="78357-201">0x0-o computador está saindo do modo ausente.</span><span class="sxs-lookup"><span data-stu-id="78357-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="78357-202">0x1-o computador está entrando no modo ausente.</span><span class="sxs-lookup"><span data-stu-id="78357-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78357-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78357-203">Requirements</span></span>



| <span data-ttu-id="78357-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="78357-204">Requirement</span></span> | <span data-ttu-id="78357-205">Valor</span><span class="sxs-lookup"><span data-stu-id="78357-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78357-206">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78357-206">Header</span></span><br/> | <dl> <span data-ttu-id="78357-207"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="78357-207"><dt>WinNT.h</dt></span></span> </dl> |



 

