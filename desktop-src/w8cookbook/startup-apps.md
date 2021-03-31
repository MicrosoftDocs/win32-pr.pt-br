---
title: Aplicativos de inicialização
description: Aplicativos de inicialização
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- aplicativo de inicialização
- tarefa em segundo plano
- Executar chave
- RunOnce
- pasta de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103642932"
---
# <a name="startup-apps"></a><span data-ttu-id="9b050-108">Aplicativos de inicialização</span><span class="sxs-lookup"><span data-stu-id="9b050-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="9b050-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="9b050-109">Platform</span></span>

<span data-ttu-id="9b050-110">**Clientes**   do   Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b050-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="9b050-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b050-111">Description</span></span>

<span data-ttu-id="9b050-112">Uma das grandes opções com o Windows é a capacidade de iluminar vários fatores forma, desde desktops e laptops tradicionais até tablets de baixa potência.</span><span class="sxs-lookup"><span data-stu-id="9b050-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="9b050-113">Para garantir que nossos clientes mútuos tenham uma ótima experiência em qualquer fator forma que escolherem com o Windows, duas métricas de sucesso-chave que precisam ser atendidas aumentam a vida útil da bateria e a excelente capacidade de resposta do PC.</span><span class="sxs-lookup"><span data-stu-id="9b050-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="9b050-114">Para conseguir isso, foram feitas melhorias em várias áreas do Windows, incluindo ciclo de vida do processo, Estados de suspensão e aplicativos de inicialização (aplicativos com inicialização automatizada após a inicialização do computador).</span><span class="sxs-lookup"><span data-stu-id="9b050-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="9b050-115">Este tópico destaca alguns dos impactos que os aplicativos de inicialização têm em um dispositivo Windows e fornece orientação aos desenvolvedores (ISV/IHV) e aos OEMs para reconsiderar os padrões de uso dos aplicativos de inicialização a fim de melhorar a vida útil da bateria e a capacidade de resposta para nossos clientes mútuos.</span><span class="sxs-lookup"><span data-stu-id="9b050-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="9b050-116">Ele também descreve as alterações no Windows que colocam os usuários no controle de determinar qual dos aplicativos de inicialização realmente são executados.</span><span class="sxs-lookup"><span data-stu-id="9b050-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="9b050-117">Os aplicativos da Windows Store são projetados para aderir a novos padrões de consumo e capacidade de resposta da bateria, e o Windows gerencia seu ciclo de vida, suspendendo e/ou encerrando-os.</span><span class="sxs-lookup"><span data-stu-id="9b050-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="9b050-118">No entanto, os aplicativos da área de trabalho projetados para versões anteriores do Windows não foram necessariamente projetados para preservar a vida útil da bateria ou serem sensíveis à atividade do usuário e podem afetar a capacidade de resposta do sistema (por exemplo, quando um aplicativo envia uma pulsação de 1 segundo regular para verificar se há atualizações ou pré-instalar antecipadamente a memória, caso precise dela mais tarde).</span><span class="sxs-lookup"><span data-stu-id="9b050-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="9b050-119">Isso pode criar uma experiência ruim para o usuário que compra um Tablet PC com uma expectativa de vida útil de bateria e semanas de espera, mas descobre que a vida útil da bateria do Tablet s não atinge essas metas.</span><span class="sxs-lookup"><span data-stu-id="9b050-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="9b050-120">Além disso, como os aplicativos de inicialização são executados em segundo plano, o número de aplicativos em execução no sistema pode ser significativamente mais do que o usuário está ciente e afetar a capacidade de resposta do sistema.</span><span class="sxs-lookup"><span data-stu-id="9b050-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="9b050-121">Os aplicativos de inicialização são classificados para incluir aqueles que aproveitam esses mecanismos para iniciar:</span><span class="sxs-lookup"><span data-stu-id="9b050-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="9b050-122">Executar chaves do registro (HKLM, HKCU, nós do WOW64 incluídos)</span><span class="sxs-lookup"><span data-stu-id="9b050-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="9b050-123">Chaves do registro RunOnce</span><span class="sxs-lookup"><span data-stu-id="9b050-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="9b050-124">Pastas de inicialização no menu Iniciar para locais por usuário e público</span><span class="sxs-lookup"><span data-stu-id="9b050-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="9b050-125">Novas funcionalidades foram adicionadas ao Windows para garantir que os usuários finais estejam sempre no controle dos aplicativos executados em seus sistemas.</span><span class="sxs-lookup"><span data-stu-id="9b050-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="9b050-126">A guia inicialização no Gerenciador de tarefas mostra uma lista de aplicativos de inicialização, juntamente com controles que permitem aos usuários desabilitar os aplicativos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9b050-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="9b050-127">Para ajudar os usuários a determinar o que desabilitar, o Gerenciador de tarefas exibe uma medida de cada impacto de s do aplicativo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9b050-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="9b050-128">O impacto é avaliado com base na CPU e no uso do disco s do aplicativo na inicialização.</span><span class="sxs-lookup"><span data-stu-id="9b050-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="9b050-129">Os valores de impacto são determinados pela aplicação destes critérios:</span><span class="sxs-lookup"><span data-stu-id="9b050-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="9b050-130">**Alto impacto**   Aplicativos que usam mais de um segundo de tempo de CPU ou mais de 3 MB de e/s de disco na inicialização</span><span class="sxs-lookup"><span data-stu-id="9b050-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="9b050-131">**Impacto médio**   Aplicativos que usam 300 MS-1000 MS de tempo de CPU ou 300 KB-3 MB de e/s de disco</span><span class="sxs-lookup"><span data-stu-id="9b050-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="9b050-132">**Baixo impacto**   Aplicativos que usam menos de 300 MS de tempo de CPU e menos de 300 KB de e/s de disco</span><span class="sxs-lookup"><span data-stu-id="9b050-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="9b050-133">A Microsoft fornece ferramentas para ajudar os desenvolvedores de aplicativos a avaliar, analisar e tomar medidas para reduzir o impacto na inicialização e melhorar a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b050-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="9b050-134">O kit de avaliação e implantação fornece a capacidade de executar uma avaliação de desempenho de inicialização e medir o impacto dos aplicativos executados na inicialização.</span><span class="sxs-lookup"><span data-stu-id="9b050-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="9b050-135">Os resultados da avaliação contêm informações detalhadas de análise e correção, quando aplicável, para os componentes de impacto superior na inicialização do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b050-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="9b050-136">Usando o analisador de desempenho do Windows, os desenvolvedores de aplicativos podem executar uma análise profunda para encontrar a causa raiz do impacto no desempenho e melhorar o desempenho de inicialização do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b050-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="9b050-137">Instale o Windows ADK [aqui](/previous-versions/windows/hh825494(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="9b050-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="9b050-138">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="9b050-138">Guidance</span></span>

<span data-ttu-id="9b050-139">Os aplicativos de inicialização abrangem várias categorias, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b050-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="9b050-140">Um conjunto de recomendações para desenvolvedores é mapeado para as categorias de aplicativos de inicialização para se alinhar com as alterações funcionais do Windows descritas acima.</span><span class="sxs-lookup"><span data-stu-id="9b050-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="9b050-141">Categorias de aplicativos de inicialização</span><span class="sxs-lookup"><span data-stu-id="9b050-141">Startup Apps Categories</span></span>

<span data-ttu-id="9b050-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b050-142">Description</span></span>

<span data-ttu-id="9b050-143">Recomendação</span><span class="sxs-lookup"><span data-stu-id="9b050-143">Recommendation</span></span>

<span data-ttu-id="9b050-144">**Atualizadores**</span><span class="sxs-lookup"><span data-stu-id="9b050-144">**Updaters**</span></span>

<span data-ttu-id="9b050-145">Monitorar e atualizar usuários para atualizações online</span><span class="sxs-lookup"><span data-stu-id="9b050-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="9b050-146">**Tarefa de manutenção**</span><span class="sxs-lookup"><span data-stu-id="9b050-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="9b050-147">Todas as atualizações devem ser tarefas de manutenção, sem nenhum requisito de interação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b050-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="9b050-148">Os aplicativos devem apenas se atualizar silenciosamente e reverter em caso de falha</span><span class="sxs-lookup"><span data-stu-id="9b050-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="9b050-149">$ {ROWSPAN2} $**assistência de hardware**$ {remover} $</span><span class="sxs-lookup"><span data-stu-id="9b050-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="9b050-150">Pontos de acesso alternativos</span><span class="sxs-lookup"><span data-stu-id="9b050-150">Alternative Access Points</span></span>

<span data-ttu-id="9b050-151">Fornecer acesso a recursos e aplicativos do Windows que são acessíveis por meio de outros pontos de acesso no Windows</span><span class="sxs-lookup"><span data-stu-id="9b050-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="9b050-152">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9b050-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="9b050-153">A chave é reduzir os recursos duplicados existentes no Windows</span><span class="sxs-lookup"><span data-stu-id="9b050-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="9b050-154">Notificadores</span><span class="sxs-lookup"><span data-stu-id="9b050-154">Notifiers</span></span>

<span data-ttu-id="9b050-155">Fornecer aos usuários notificações sobre seus dispositivos</span><span class="sxs-lookup"><span data-stu-id="9b050-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="9b050-156">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9b050-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="9b050-157">O Windows fornece notificações aos usuários sobre seus dispositivos</span><span class="sxs-lookup"><span data-stu-id="9b050-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="9b050-158">**Pré-iniciadores**</span><span class="sxs-lookup"><span data-stu-id="9b050-158">**Pre-launchers**</span></span>

<span data-ttu-id="9b050-159">Algumas das atividades preliminares necessárias para os aplicativos são descarregadas em um aplicativo de inicialização durante o logon do usuário</span><span class="sxs-lookup"><span data-stu-id="9b050-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="9b050-160">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9b050-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="9b050-161">O Windows 8 é otimizado para uma experiência rápida para lançamentos de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9b050-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="9b050-162">$ {ROWSPAN4} $**Utility**$ {remover} $</span><span class="sxs-lookup"><span data-stu-id="9b050-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="9b050-163">Sincronização de PC</span><span class="sxs-lookup"><span data-stu-id="9b050-163">PC Sync</span></span>

<span data-ttu-id="9b050-164">Fornecer funcionalidade de sincronização em vários sistemas</span><span class="sxs-lookup"><span data-stu-id="9b050-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="9b050-165">**Inicialização** (atualizações em potencial na versão beta)</span><span class="sxs-lookup"><span data-stu-id="9b050-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="9b050-166">Recuperação de & de backup</span><span class="sxs-lookup"><span data-stu-id="9b050-166">Backup & Recovery</span></span>

<span data-ttu-id="9b050-167">Ponto de entrada para salvar e restaurar o estado de arquivos, configurações ou sistemas inteiros</span><span class="sxs-lookup"><span data-stu-id="9b050-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="9b050-168">**Aplicativo da Windows Store para interface com os usuários**</span><span class="sxs-lookup"><span data-stu-id="9b050-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="9b050-169">Telemetria</span><span class="sxs-lookup"><span data-stu-id="9b050-169">Telemetry</span></span>

<span data-ttu-id="9b050-170">Coletar e enviar informações sobre a experiência do usuário e o ambiente</span><span class="sxs-lookup"><span data-stu-id="9b050-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="9b050-171">**Tarefa de manutenção**</span><span class="sxs-lookup"><span data-stu-id="9b050-171">**Maintenance Task**</span></span>

<span data-ttu-id="9b050-172">Monitoramento de PC</span><span class="sxs-lookup"><span data-stu-id="9b050-172">PC Monitoring</span></span>

<span data-ttu-id="9b050-173">Fornecer monitoramento e notificações de estado do sistema não solicitados que duplicam a funcionalidade de caixa de entrada existente</span><span class="sxs-lookup"><span data-stu-id="9b050-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="9b050-174">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9b050-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="9b050-175">A chave é reduzir os recursos duplicados existentes no Windows</span><span class="sxs-lookup"><span data-stu-id="9b050-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="9b050-176">$ {ROWSPAN2} $**Security**$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="9b050-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="9b050-177">Filtros de & de controle dos pais</span><span class="sxs-lookup"><span data-stu-id="9b050-177">Parental Control & Filters</span></span>

<span data-ttu-id="9b050-178">Impor regras e restrições estabelecidas para acesso e uso da Internet</span><span class="sxs-lookup"><span data-stu-id="9b050-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="9b050-179">**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="9b050-179">**Startup**</span></span>

<span data-ttu-id="9b050-180">Configuração e gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9b050-180">Configuration & Management</span></span>

<span data-ttu-id="9b050-181">Permitir que os usuários controlem as opções de diagnóstico e correção para o monitoramento de segurança do sistema notificar usuários de conclusões e ações de segurança</span><span class="sxs-lookup"><span data-stu-id="9b050-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="9b050-182">**Aplicativo da Windows Store para interface com os usuários**</span><span class="sxs-lookup"><span data-stu-id="9b050-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="9b050-183">**Comunicação & Internet** (im & VoIP)</span><span class="sxs-lookup"><span data-stu-id="9b050-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="9b050-184">Enviar e receber mensagens e chamadas</span><span class="sxs-lookup"><span data-stu-id="9b050-184">Send and receive messages and calls</span></span>

<span data-ttu-id="9b050-185">**Aplicativo da Windows Store**</span><span class="sxs-lookup"><span data-stu-id="9b050-185">**Windows Store app**</span></span>

<span data-ttu-id="9b050-186">**Música & MP3**</span><span class="sxs-lookup"><span data-stu-id="9b050-186">**Music & MP3**</span></span>

<span data-ttu-id="9b050-187">Reproduzir, armazenar e gerenciar música</span><span class="sxs-lookup"><span data-stu-id="9b050-187">Play, store, and manage music</span></span>

<span data-ttu-id="9b050-188">**Aplicativo da Windows Store**</span><span class="sxs-lookup"><span data-stu-id="9b050-188">**Windows Store app**</span></span>

<span data-ttu-id="9b050-189">**Vídeo de & de fotos**</span><span class="sxs-lookup"><span data-stu-id="9b050-189">**Photo & Video**</span></span>

<span data-ttu-id="9b050-190">Detecte, registre, processe, armazene e gerencie fotos e vídeos</span><span class="sxs-lookup"><span data-stu-id="9b050-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="9b050-191">**Aplicativo da Windows Store**</span><span class="sxs-lookup"><span data-stu-id="9b050-191">**Windows Store app**</span></span>

<span data-ttu-id="9b050-192">**Jogos para PCs**</span><span class="sxs-lookup"><span data-stu-id="9b050-192">**PC Gaming**</span></span>

<span data-ttu-id="9b050-193">Iniciar jogos em vários domínios</span><span class="sxs-lookup"><span data-stu-id="9b050-193">Launch games across various domains</span></span>

<span data-ttu-id="9b050-194">**Aplicativo da Windows Store**</span><span class="sxs-lookup"><span data-stu-id="9b050-194">**Windows Store app**</span></span>

<span data-ttu-id="9b050-195">**Venda & anúncio**</span><span class="sxs-lookup"><span data-stu-id="9b050-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="9b050-196">Chame atenção para produtos e serviços disponíveis para compra</span><span class="sxs-lookup"><span data-stu-id="9b050-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="9b050-197">**Remover**</span><span class="sxs-lookup"><span data-stu-id="9b050-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="9b050-198">As diretrizes de aplicativos de acessibilidade são cobertas por engajamentos diretos separados com ISVs.</span><span class="sxs-lookup"><span data-stu-id="9b050-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="9b050-199">Consulte [*programação para facilidade de acesso*](../winauto/ease-of-access---assistive-technology-registration.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9b050-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="9b050-200">**Aplicativos da Windows Store**</span><span class="sxs-lookup"><span data-stu-id="9b050-200">**Windows Store apps**</span></span>

<span data-ttu-id="9b050-201">Os aplicativos da Windows Store aprimoram a experiência do usuário introduzindo um espaço do Windows com novas coordenadas: um novo modelo de aplicativo, uma nova interface do usuário e uma Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9b050-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="9b050-202">Essas opções de estrutura de idioma e apresentação estão disponíveis para o desenvolvimento de aplicativos da Windows Store:</span><span class="sxs-lookup"><span data-stu-id="9b050-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="9b050-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="9b050-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="9b050-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="9b050-204">XAML/C#</span></span>
-   <span data-ttu-id="9b050-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="9b050-205">XAML/C++</span></span>

<span data-ttu-id="9b050-206">As informações agregadas para o desenvolvimento de aplicativos da Windows Store estão disponíveis no [centro de desenvolvimento do Windows](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="9b050-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="9b050-207">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="9b050-207">Examples:</span></span>

-   <span data-ttu-id="9b050-208">[Desenvolvendo jogos da Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b050-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="9b050-209">[Desenvolvendo aplicativos da Windows Store que usam mídia](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b050-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="9b050-210">**Tarefas de manutenção automática**</span><span class="sxs-lookup"><span data-stu-id="9b050-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="9b050-211">A atividade de plano de fundo periódica deve ser projetada como tarefas de manutenção automáticas.</span><span class="sxs-lookup"><span data-stu-id="9b050-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="9b050-212">Eles estão agendados no tempo ocioso do sistema para aumentar a capacidade de resposta e a eficiência energética dos computadores Windows.</span><span class="sxs-lookup"><span data-stu-id="9b050-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="9b050-213">As tarefas de manutenção podem ser criadas e configuradas por um aplicativo de área de trabalho no momento da instalação, usando o SDK da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b050-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="9b050-214">Consulte o tópico manutenção automática a seguir para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9b050-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="9b050-215">Recursos</span><span class="sxs-lookup"><span data-stu-id="9b050-215">Resources</span></span>

-   [<span data-ttu-id="9b050-216">Diretrizes de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9b050-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="9b050-217">Central de Desenvolvimento do Windows</span><span class="sxs-lookup"><span data-stu-id="9b050-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="9b050-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b050-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

