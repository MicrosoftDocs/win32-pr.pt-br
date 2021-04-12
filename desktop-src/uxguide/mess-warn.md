---
title: Mensagens de aviso
description: Uma mensagem de aviso é uma caixa de diálogo modal, uma mensagem in-loco, uma notificação ou um balão que alerta o usuário sobre uma condição que pode causar um problema no futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297866"
---
# <a name="warning-messages"></a><span data-ttu-id="e1ab8-103">Mensagens de aviso</span><span class="sxs-lookup"><span data-stu-id="e1ab8-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="e1ab8-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="e1ab8-105">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="e1ab8-106">Uma mensagem de aviso é uma caixa de diálogo modal, uma mensagem in-loco, uma notificação ou um balão que alerta o usuário sobre uma condição que pode causar um problema no futuro.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![captura de tela de uma mensagem de aviso típica](images/mess-warn-image1.png)

<span data-ttu-id="e1ab8-108">Uma mensagem de aviso modal típica.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-108">A typical modal warning message.</span></span>

<span data-ttu-id="e1ab8-109">A característica fundamental dos avisos é que eles envolvem o risco de perder um ou mais dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="e1ab8-110">Um ativo valioso, como importante finanças ou outros dados.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="e1ab8-111">Integridade ou acesso do sistema.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-111">System access or integrity.</span></span>
-   <span data-ttu-id="e1ab8-112">Privacidade ou controle sobre informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="e1ab8-113">Tempo do usuário (um valor significativo, como 30 segundos ou mais).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="e1ab8-114">Por outro lado, uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja prosseguir com uma ação.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="e1ab8-115">Alguns tipos de avisos são apresentados como confirmações e, nesse caso, as diretrizes de confirmação também se aplicam.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="e1ab8-116">**Observação:** As diretrizes relacionadas [a caixas de diálogo](win-dialog-box.md), [confirmações](mess-confirm.md),[ícones padrão](vis-std-icons.md)de [mensagens de erro](mess-error.md), [notificações](mess-notif.md)e [layout](vis-layout.md) são apresentadas em artigos separados.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="e1ab8-117">Esta é a interface do usuário correta?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-117">Is this the right user interface?</span></span>

<span data-ttu-id="e1ab8-118">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="e1ab8-119">**O usuário está sendo alertado sobre uma condição que pode causar um problema no futuro?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="e1ab8-120">Caso contrário, a mensagem não é um aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="e1ab8-121">**A interface do usuário está apresentando um erro ou problema que já ocorreu?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="e1ab8-122">Nesse caso, use uma mensagem de erro em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="e1ab8-123">**Os usuários provavelmente executarão uma ação ou alterarão seu comportamento como resultado da mensagem?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="e1ab8-124">Caso contrário, a condição não justifica a interrupção do usuário para que seja melhor suprimir o aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="e1ab8-125">**A condição é o resultado direto de uma ação iniciada pelo usuário?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="e1ab8-126">Caso contrário, considere o uso de [notificações de eventos não críticas](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="e1ab8-127">**A condição é uma condição especial em um controle?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="e1ab8-128">Nesse caso, use um [balão](ctrl-balloons.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ab8-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="e1ab8-129">**Para confirmações, o usuário está prestes a executar uma ação arriscada?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="e1ab8-130">Nesse caso, um aviso será apropriado se a ação tiver consequências significativas ou não puder ser facilmente desfeita.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="e1ab8-131">**Para outros tipos de avisos, o usuário precisa agir agora ou no futuro imediato?**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="e1ab8-132">Não exiba avisos se os usuários puderem continuar a trabalhar de maneira produtiva sem problemas imediatos.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="e1ab8-133">Adie o aviso até que a condição seja mais imediata e relevante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="e1ab8-134">Conceitos de design</span><span class="sxs-lookup"><span data-stu-id="e1ab8-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="e1ab8-135">Evitar aviso prévio</span><span class="sxs-lookup"><span data-stu-id="e1ab8-135">Avoid overwarning</span></span>

<span data-ttu-id="e1ab8-136">Nós alertamos os programas do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="e1ab8-137">O programa típico do Windows tem avisos aparentemente em qualquer lugar, avisando sobre coisas que têm pouco significado.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="e1ab8-138">Em alguns programas, quase todas as perguntas são apresentadas como um aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="e1ab8-139">A deadvertência faz com que o uso de um programa seja semelhante a uma atividade perigosa e se reduz de problemas realmente significativos.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="e1ab8-140">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-140">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-141">captura de tela de uma mensagem de aviso desnecessária</span><span class="sxs-lookup"><span data-stu-id="e1ab8-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="e1ab8-142">O alerta faz com que seu programa sinta-se perigoso e pareça que foi projetado por advogados.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="e1ab8-143">A mera possibilidade de perda de dados ou um problema futuro sozinho é insuficiente para chamar um aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="e1ab8-144">Além disso, os resultados indesejáveis devem ser inesperados ou indesejados e não facilmente corrigidos.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="e1ab8-145">Caso contrário, praticamente qualquer erro de usuário poderia ser interpretado para resultar em perda de dados ou em um possível problema de algum tipo e merecer um aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="e1ab8-146">Características de bons avisos</span><span class="sxs-lookup"><span data-stu-id="e1ab8-146">Characteristics of good warnings</span></span>

<span data-ttu-id="e1ab8-147">Bons avisos:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-147">Good warnings:</span></span>

-   <span data-ttu-id="e1ab8-148">**Envolva riscos.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-148">**Involve risk.**</span></span> <span data-ttu-id="e1ab8-149">Bons avisos alertam os usuários de algo significativo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="e1ab8-150">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-150">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-151">captura de tela de ' deseja sair? '</span><span class="sxs-lookup"><span data-stu-id="e1ab8-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="e1ab8-152">warning</span><span class="sxs-lookup"><span data-stu-id="e1ab8-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="e1ab8-153">E daí?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-153">So what?</span></span> <span data-ttu-id="e1ab8-154">Essa confirmação pressupõe que os usuários geralmente saem de programas por acidente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="e1ab8-155">**Tenha relevância imediata.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-155">**Have immediate relevance.**</span></span> <span data-ttu-id="e1ab8-156">Não apenas os usuários precisam se preocupar, eles precisam se preocupar agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="e1ab8-157">Os usuários normalmente não estão interessados em problemas que possam ter mais tarde, contanto que possam fazer seu trabalho agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="e1ab8-158">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-158">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-159">captura de tela de aviso de bateria-pouco em três horas</span><span class="sxs-lookup"><span data-stu-id="e1ab8-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="e1ab8-160">Nesse caso, é melhor apenas avisar o usuário em três horas.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="e1ab8-161">**Levar à ação.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-161">**Lead to action.**</span></span> <span data-ttu-id="e1ab8-162">Há algo que os usuários devem fazer ou estar cientes como resultado do aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="e1ab8-163">Talvez eles devam executar uma ação agora ou em algum momento no futuro imediato.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="e1ab8-164">Talvez eles executem uma tarefa de forma diferente como resultado.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="e1ab8-165">A consequência de ignorar o aviso deve ser clara.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="e1ab8-166">Avisos sem ações apenas fazem com que os usuários se sintam paranóicos.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="e1ab8-167">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-167">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-168">aviso de captura de tela do ' Live Messenger em execução '</span><span class="sxs-lookup"><span data-stu-id="e1ab8-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="e1ab8-169">Por que essa notificação é um aviso?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-169">Why is this notification a warning?</span></span> <span data-ttu-id="e1ab8-170">O que os usuários devem fazer (ao contrário de se preocupar)?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="e1ab8-171">**Não são óbvias.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-171">**Are not obvious.**</span></span> <span data-ttu-id="e1ab8-172">Não exiba um aviso para declarar a consequência óbvia de uma ação.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="e1ab8-173">Por exemplo, suponha que os usuários compreendam as consequências de não concluir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="e1ab8-174">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-174">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-175">captura de tela de você deseja sair do assistente? alerta</span><span class="sxs-lookup"><span data-stu-id="e1ab8-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="e1ab8-176">Cancelar um assistente incompleto significa que a tarefa não é concluída... Quem sabia?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="e1ab8-177">**Ocorrem com pouca frequência.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-177">**Occur infrequently.**</span></span> <span data-ttu-id="e1ab8-178">Os avisos constantes se tornam ineficientes e irritantes rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="e1ab8-179">Os usuários geralmente se concentram em se livrar do aviso do que resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="e1ab8-180">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-180">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-181">captura de tela do aviso "atualizar assinaturas de vírus"</span><span class="sxs-lookup"><span data-stu-id="e1ab8-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="e1ab8-182">Os usuários têm mais probabilidade de se concentrar em se livrar do aviso do que corrigir o problema subjacente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="e1ab8-183">Uma mensagem que não tem essas características ainda pode ser uma boa mensagem, mas não é um bom aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="e1ab8-184">Determinar o tipo de mensagem apropriado</span><span class="sxs-lookup"><span data-stu-id="e1ab8-184">Determine the appropriate message type</span></span>

<span data-ttu-id="e1ab8-185">Alguns problemas podem ser apresentados como erro, aviso ou informações, dependendo da ênfase e da formulação.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="e1ab8-186">Por exemplo, suponha que uma página da Web não possa carregar um controle ActiveX não assinado com base na configuração atual do Windows Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="e1ab8-187">**Ao.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-187">**Error.**</span></span> <span data-ttu-id="e1ab8-188">"Esta página não pode carregar um controle ActiveX não assinado".</span><span class="sxs-lookup"><span data-stu-id="e1ab8-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="e1ab8-189">(Fraseada como um problema existente.)</span><span class="sxs-lookup"><span data-stu-id="e1ab8-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="e1ab8-190">**Alerta.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-190">**Warning.**</span></span> <span data-ttu-id="e1ab8-191">"Esta página pode não se comportar conforme o esperado porque o Windows Internet Explorer não está configurado para carregar controles ActiveX não assinados."</span><span class="sxs-lookup"><span data-stu-id="e1ab8-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="e1ab8-192">ou "permitir que esta página instale um controle ActiveX não assinado?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="e1ab8-193">Fazer isso de fontes não confiáveis pode prejudicar seu computador. "</span><span class="sxs-lookup"><span data-stu-id="e1ab8-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="e1ab8-194">(Fraseada como condições que podem causar problemas futuros.)</span><span class="sxs-lookup"><span data-stu-id="e1ab8-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="e1ab8-195">**Divulgação.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-195">**Information.**</span></span> <span data-ttu-id="e1ab8-196">"Você configurou o Windows Internet Explorer para bloquear controles ActiveX não assinados".</span><span class="sxs-lookup"><span data-stu-id="e1ab8-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="e1ab8-197">(Fraseada como uma declaração de fato).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="e1ab8-198">**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="e1ab8-199">Normalmente, se um problema impedir que o usuário Continue, você deverá apresentá-lo como um erro; Se o usuário puder continuar, apresente-o como um aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="e1ab8-200">Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e, em seguida, escolha um ícone ([padrão](vis-std-icons.md) ou de outra forma) que corresponda ao texto.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="e1ab8-201">O texto da instrução principal e os ícones sempre devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="e1ab8-202">Ser específico</span><span class="sxs-lookup"><span data-stu-id="e1ab8-202">Be specific</span></span>

<span data-ttu-id="e1ab8-203">Os avisos são mais atraentes quando as seguintes informações são específicas e claras:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="e1ab8-204">A origem do aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-204">The source of the warning.</span></span>
-   <span data-ttu-id="e1ab8-205">A condição específica e o problema em potencial.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="e1ab8-206">O que o usuário deve fazer sobre ele.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-206">What the user should do about it.</span></span>
-   <span data-ttu-id="e1ab8-207">O que acontecerá se o usuário não fizer nada.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="e1ab8-208">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-208">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-209">captura de tela de aviso vaga de risco significativo</span><span class="sxs-lookup"><span data-stu-id="e1ab8-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="e1ab8-210">Neste exemplo, qual é o problema em potencial?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="e1ab8-211">O que o usuário deve fazer, além de não usar o projetor pela rede?</span><span class="sxs-lookup"><span data-stu-id="e1ab8-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="e1ab8-212">Sem informações mais específicas, tudo o que o usuário pode fazer é uma boa idéia de continuar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="e1ab8-213">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-213">**Correct:**</span></span>

![<span data-ttu-id="e1ab8-214">captura de tela de aviso de problema e consequências</span><span class="sxs-lookup"><span data-stu-id="e1ab8-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="e1ab8-215">Neste exemplo, o problema e as consequências estão claros.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="e1ab8-216">Às vezes, há um problema potencial legítimo que vale a pena informar os usuários sobre, mas a solução e as consequências não são conhecidas com certeza.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="e1ab8-217">Em vez de dar um aviso vaga, seja específico, fornecendo as informações mais prováveis ou o exemplo mais comum.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="e1ab8-218">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-218">**Correct:**</span></span>

![<span data-ttu-id="e1ab8-219">captura de tela de avisos e soluções de erro de rede</span><span class="sxs-lookup"><span data-stu-id="e1ab8-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="e1ab8-220">Neste exemplo, o aviso é feito específico fornecendo a solução mais provável.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="e1ab8-221">No entanto, nesses casos, use palavras que indiquem que há outras possibilidades.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="e1ab8-222">Caso contrário, os usuários podem ser enganam.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="e1ab8-223">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-223">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-224">captura de tela do aviso de cabo de rede não conectado</span><span class="sxs-lookup"><span data-stu-id="e1ab8-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="e1ab8-225">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-225">**Correct:**</span></span>

![<span data-ttu-id="e1ab8-226">aviso de captura de tela de cabo pode ser desconectado</span><span class="sxs-lookup"><span data-stu-id="e1ab8-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="e1ab8-227">No exemplo incorreto, os usuários ficarão confusos se o cabo estiver claramente conectado.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="e1ab8-228">**Se você fizer apenas duas coisas...**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="e1ab8-229">Não avisar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-229">Don't overwarn.</span></span> <span data-ttu-id="e1ab8-230">Limite os avisos a condições que envolvem risco e são imediatamente relevantes, acionáveis, não óbvios e pouco frequentes.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="e1ab8-231">Caso contrário, remova ou reformule a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="e1ab8-232">Forneça informações específicas e úteis.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="e1ab8-233">Padrões de uso</span><span class="sxs-lookup"><span data-stu-id="e1ab8-233">Usage patterns</span></span>

<span data-ttu-id="e1ab8-234">Os avisos têm vários padrões de uso:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1ab8-235"><strong>Reconhecimento</strong></span><span class="sxs-lookup"><span data-stu-id="e1ab8-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="e1ab8-236">Torne o usuário ciente de uma condição ou um possível problema, mas talvez o usuário não precise fazer nada agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="e1ab8-237">Exemplos de avisos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="e1ab8-238">Os avisos de conscientização têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="e1ab8-239"><strong>Instrução principal:</strong> Descreva a condição ou o problema potencial.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="e1ab8-240"><strong>Instrução complementar:</strong> Explique a implicação e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="e1ab8-241"><strong>Botões de confirmação:</strong> Inclui.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ab8-242"><strong>Prevenção de erros</strong></span><span class="sxs-lookup"><span data-stu-id="e1ab8-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="e1ab8-243">Torne o usuário ciente de informações que podem impedir um problema, especialmente ao fazer escolhas.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="e1ab8-244">Os avisos de prevenção de erros são apresentados melhor usando um ícone de aviso in-loco e um texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="e1ab8-245">Exemplos de avisos de prevenção de erros.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ab8-246"><strong>Problema iminente</strong></span><span class="sxs-lookup"><span data-stu-id="e1ab8-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="e1ab8-247">O usuário precisa fazer algo agora para evitar um problema iminente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="e1ab8-248">Um exemplo de um aviso de problema iminente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="e1ab8-249">Os avisos de problema iminentes têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="e1ab8-250"><strong>Instrução principal:</strong> Descreva o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="e1ab8-251"><strong>Instrução complementar:</strong> Explique a condição e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="e1ab8-252"><strong>Botões de confirmação:</strong> Um botão de comando ou link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ab8-253"><strong>Confirmação de ação arriscada</strong></span><span class="sxs-lookup"><span data-stu-id="e1ab8-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="e1ab8-254">Confirme se o usuário deseja prosseguir com uma ação que tenha algum risco e não possa ser facilmente desfeito.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="e1ab8-255">Um exemplo de confirmação de ação arriscada.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="e1ab8-256">Confirmações de ações arriscadas têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="e1ab8-257"><strong>Instrução principal:</strong> Faça uma pergunta para determinar se o usuário deseja continuar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="e1ab8-258"><strong>Instrução complementar:</strong> Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="e1ab8-259"><strong>Botões de confirmação:</strong> Sim, não.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="e1ab8-260">Para obter diretrizes sobre esse padrão, consulte <a href="mess-confirm.md">confirmações</a>.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="e1ab8-261">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="e1ab8-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="e1ab8-262">Apresentação</span><span class="sxs-lookup"><span data-stu-id="e1ab8-262">Presentation</span></span>

-   <span data-ttu-id="e1ab8-263">**Escolha a interface do usuário de apresentação com base no tipo de informação:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-263">**Choose the presentation UI based on the type of information:**</span></span>



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ab8-264">**Interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-264">**User interface**</span></span><br/> | <span data-ttu-id="e1ab8-265">**Mais usado para**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-265">**Best used for**</span></span><br/>                                                                                                           |
| <span data-ttu-id="e1ab8-266">Caixas de diálogo modais</span><span class="sxs-lookup"><span data-stu-id="e1ab8-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="e1ab8-267">Avisos críticos (incluindo confirmações) que os usuários devem responder agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="e1ab8-268">No local</span><span class="sxs-lookup"><span data-stu-id="e1ab8-268">In-place</span></span><br/>           | <span data-ttu-id="e1ab8-269">Informações que podem impedir um problema, especialmente quando os usuários estão fazendo escolhas.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="e1ab8-270">Publicitária</span><span class="sxs-lookup"><span data-stu-id="e1ab8-270">Banners</span></span><br/>            | <span data-ttu-id="e1ab8-271">Informações que podem impedir um problema, especialmente quando relacionadas à conclusão de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="e1ab8-272">Notificações</span><span class="sxs-lookup"><span data-stu-id="e1ab8-272">Notifications</span></span><br/>      | <span data-ttu-id="e1ab8-273">Eventos significativos ou status que podem ser ignorados com segurança, pelo menos temporariamente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="e1ab8-274">Balões</span><span class="sxs-lookup"><span data-stu-id="e1ab8-274">Balloons</span></span><br/>           | <span data-ttu-id="e1ab8-275">Um controle está em um estado que afeta a entrada.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-275">A control is in a state that affects input.</span></span> <span data-ttu-id="e1ab8-276">Esse Estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="e1ab8-277">**Para caixas de diálogo modais:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="e1ab8-278">**Use caixas de diálogo de tarefas sempre que apropriado para obter uma aparência e um layout consistentes.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="e1ab8-279">As caixas de diálogo de tarefas exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="e1ab8-280">**Exibe apenas uma mensagem de aviso por condição.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="e1ab8-281">Por exemplo, exiba um único aviso que explique completamente uma condição em vez de descrever um detalhe por vez por mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="e1ab8-282">Exibir uma sequência de caixas de diálogo de aviso para uma única condição é confuso e irritante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="e1ab8-283">**Não exibir um aviso mais de uma vez por condição.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="e1ab8-284">Os avisos constantes se tornam ineficientes e irritantes rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="e1ab8-285">Os usuários geralmente se concentram em se livrar do aviso do que resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="e1ab8-286">Se você precisar avisar repetidamente para uma única condição, use [escalonamento progressivo](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="e1ab8-287">**Não acompanha avisos com um efeito sonoro ou um aviso sonoro.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="e1ab8-288">Fazer isso é dissonante e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="e1ab8-289">**Exceção:** Se o usuário precisar responder imediatamente, você poderá usar um efeito de som.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="e1ab8-290">Ícones</span><span class="sxs-lookup"><span data-stu-id="e1ab8-290">Icons</span></span>

-   <span data-ttu-id="e1ab8-291">Não coloque um ícone de aviso na barra de título de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="e1ab8-292">**Use um ícone de aviso.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-292">**Use a warning icon.**</span></span> <span data-ttu-id="e1ab8-293">Exceções:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-293">Exceptions:</span></span>
    -   <span data-ttu-id="e1ab8-294">Se o aviso for para um recurso que tenha um ícone, você poderá usar o ícone de recurso com uma sobreposição de aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="e1ab8-295">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-295">**Correct:**</span></span>

        ![<span data-ttu-id="e1ab8-296">captura de tela de ícone de cadeado com sobreposição de ícone de aviso</span><span class="sxs-lookup"><span data-stu-id="e1ab8-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="e1ab8-297">Neste exemplo, o ícone de recurso tem uma sobreposição de aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="e1ab8-298">Para caixas de diálogo modais com uma nota de rodapé de aviso, coloque o ícone de aviso na nota de rodapé em vez da área de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="e1ab8-299">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-299">**Correct:**</span></span>

    ![<span data-ttu-id="e1ab8-300">captura de tela do ícone de aviso na nota de rodapé da caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="e1ab8-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="e1ab8-301">Neste exemplo, a nota de rodapé tem o ícone de aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="e1ab8-302">Para obter mais diretrizes e exemplos, consulte [ícones padrão](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="e1ab8-303">Não mostrar esta mensagem novamente</span><span class="sxs-lookup"><span data-stu-id="e1ab8-303">Don't show this message again</span></span>

-   <span data-ttu-id="e1ab8-304">**Se uma caixa de diálogo de aviso precisar dessa opção, reconsidere o aviso e sua frequência.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="e1ab8-305">Se ele tem todas as características de um bom aviso (envolve risco e é imediatamente relevante, acionável, não óbvio e incomum), não deve fazer sentido para os usuários suprimirem.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="e1ab8-306">Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="e1ab8-307">Divulgação progressiva</span><span class="sxs-lookup"><span data-stu-id="e1ab8-307">Progressive disclosure</span></span>

-   <span data-ttu-id="e1ab8-308">**Se você precisar incluir informações avançadas em uma mensagem de aviso, revele-as usando botões de divulgação progressiva** (por exemplo, "mostrar detalhes").</span><span class="sxs-lookup"><span data-stu-id="e1ab8-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="e1ab8-309">Fazer isso simplifica o aviso para uso típico.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="e1ab8-310">Não oculte as informações necessárias porque os usuários talvez não as encontrem.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="e1ab8-311">**Não use "mostrar detalhes", a menos que realmente haja mais detalhes.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="e1ab8-312">Não apenas redeclare as informações existentes em um formato diferente.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="e1ab8-313">Para obter diretrizes de rotulamento, consulte [divulgação progressiva](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="e1ab8-314">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="e1ab8-314">Default values</span></span>

-   <span data-ttu-id="e1ab8-315">**Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="e1ab8-316">Texto</span><span class="sxs-lookup"><span data-stu-id="e1ab8-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="e1ab8-317">Geral</span><span class="sxs-lookup"><span data-stu-id="e1ab8-317">General</span></span>

-   <span data-ttu-id="e1ab8-318">**Remova o texto redundante.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-318">**Remove redundant text.**</span></span> <span data-ttu-id="e1ab8-319">Procure por ele em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="e1ab8-320">Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="e1ab8-321">**Não use os termos "aviso" ou "cuidado" no texto.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="e1ab8-322">Quando [usado corretamente](vis-std-icons.md), o ícone de aviso comunica suficientemente que os usuários devem continuar com cautela.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="e1ab8-323">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-323">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-324">captura de tela de uso desnecessário de aviso no texto</span><span class="sxs-lookup"><span data-stu-id="e1ab8-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="e1ab8-325">Neste exemplo, o termo "aviso" é desnecessário.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="e1ab8-326">Títulos</span><span class="sxs-lookup"><span data-stu-id="e1ab8-326">Titles</span></span>

-   <span data-ttu-id="e1ab8-327">**Use o título para identificar o comando ou recurso do qual o aviso veio.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="e1ab8-328">Exceções:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-328">Exceptions:</span></span>
    -   <span data-ttu-id="e1ab8-329">Se um aviso for exibido por vários comandos diferentes, considere usar o nome do programa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="e1ab8-330">Se esse título fosse redundante ou confuso com a instrução principal, use o nome do programa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="e1ab8-331">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-331">**Incorrect:**</span></span>

![<span data-ttu-id="e1ab8-332">captura de tela do título da caixa de diálogo de aviso de segurança</span><span class="sxs-lookup"><span data-stu-id="e1ab8-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="e1ab8-333">Neste exemplo, "aviso de segurança" não identifica o comando ou o recurso do qual veio o aviso.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="e1ab8-334">**Não use o título para explicar o que fazer na caixa de diálogo** que é a finalidade da instrução principal.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="e1ab8-335">Use [maiúsculas e minúsculas no estilo de título](glossary.md), sem pontuação final.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="e1ab8-336">Instruções principais</span><span class="sxs-lookup"><span data-stu-id="e1ab8-336">Main instructions</span></span>

-   <span data-ttu-id="e1ab8-337">A instrução principal para um aviso se baseia em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-337">The main instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e1ab8-338">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-338">**Pattern**</span></span><br/>               | <span data-ttu-id="e1ab8-339">**Instrução principal**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-339">**Main instruction**</span></span><br/>                                      |
| <span data-ttu-id="e1ab8-340">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="e1ab8-340">Awareness</span></span><br/>                 | <span data-ttu-id="e1ab8-341">Descreva a condição ou o problema potencial.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="e1ab8-342">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="e1ab8-342">Imminent problem</span></span><br/>          | <span data-ttu-id="e1ab8-343">Descreva o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="e1ab8-344">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="e1ab8-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="e1ab8-345">Faça uma pergunta para determinar se o usuário deseja continuar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="e1ab8-346">captura de tela de uma notificação de bateria fraca</span><span class="sxs-lookup"><span data-stu-id="e1ab8-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="e1ab8-347">Neste exemplo, a notificação de bateria fraca é um aviso de conscientização, portanto, a instrução principal descreve a condição.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="e1ab8-348">captura de tela de alterar a bateria imediatamente aviso</span><span class="sxs-lookup"><span data-stu-id="e1ab8-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="e1ab8-349">Neste exemplo, a caixa de diálogo de bateria fraca é um problema iminente, portanto, a instrução principal descreve o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="e1ab8-350">**Seja conciso Use apenas uma única frase completa.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="e1ab8-351">Remova a instrução principal para as informações essenciais.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="e1ab8-352">Se você precisar explicar algo mais, use uma instrução complementar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="e1ab8-353">**Use palavras como "Now" e "imediatamente" se o usuário precisar agir imediatamente.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="e1ab8-354">Não use essas palavras se não houver urgência.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="e1ab8-355">**Seja específico se houver objetos envolvidos, forneça seus nomes completos.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="e1ab8-356">Use [a capitalização no estilo de frase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="e1ab8-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="e1ab8-357">Instruções complementares</span><span class="sxs-lookup"><span data-stu-id="e1ab8-357">Supplemental instructions</span></span>

-   <span data-ttu-id="e1ab8-358">A instrução complementar para um aviso se baseia em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ab8-359">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-359">**Pattern**</span></span><br/>               | <span data-ttu-id="e1ab8-360">**Instrução complementar**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-360">**Supplemental instruction**</span></span><br/>                                            |
| <span data-ttu-id="e1ab8-361">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="e1ab8-361">Awareness</span></span><br/>                 | <span data-ttu-id="e1ab8-362">Explique a implicação e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="e1ab8-363">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="e1ab8-363">Imminent problem</span></span><br/>          | <span data-ttu-id="e1ab8-364">Explique a condição e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="e1ab8-365">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="e1ab8-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="e1ab8-366">Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="e1ab8-367">**Não repita a instrução principal com uma palavra ligeiramente diferente.**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="e1ab8-368">Em vez disso, omita a instrução complementar se não houver mais a adicionar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="e1ab8-369">Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="e1ab8-370">Botões de confirmação</span><span class="sxs-lookup"><span data-stu-id="e1ab8-370">Commit buttons</span></span>

-   <span data-ttu-id="e1ab8-371">Para caixas de diálogo de aviso, os botões de confirmação se baseiam em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ab8-372">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-372">**Pattern**</span></span><br/>               | <span data-ttu-id="e1ab8-373">**Botões de confirmação**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-373">**Commit buttons**</span></span><br/>                                                                                   |
| <span data-ttu-id="e1ab8-374">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="e1ab8-374">Awareness</span></span><br/>                 | <span data-ttu-id="e1ab8-375">Fechar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-375">Close.</span></span> <span data-ttu-id="e1ab8-376">Não use OK porque ele sugere que problemas potenciais estão OK.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="e1ab8-377">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="e1ab8-377">Imminent problem</span></span><br/>          | <span data-ttu-id="e1ab8-378">Um botão de comando ou link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="e1ab8-379">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="e1ab8-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="e1ab8-380">Sim, não.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="e1ab8-381">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="e1ab8-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="e1ab8-382">captura de tela da caixa de diálogo de aviso com o botão OK</span><span class="sxs-lookup"><span data-stu-id="e1ab8-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="e1ab8-383">Os problemas não estão OK, portanto, use fechar.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="e1ab8-384">Documentação</span><span class="sxs-lookup"><span data-stu-id="e1ab8-384">Documentation</span></span>

<span data-ttu-id="e1ab8-385">Ao fazer referência a avisos:</span><span class="sxs-lookup"><span data-stu-id="e1ab8-385">When referring to warnings:</span></span>

-   <span data-ttu-id="e1ab8-386">Se o aviso faz uma pergunta, consulte um aviso por sua pergunta; caso contrário, use a instrução principal.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="e1ab8-387">Se a pergunta ou a instrução principal for longa ou detalhada, resuma-a.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="e1ab8-388">Se necessário, você pode se referir a uma caixa de diálogo de aviso como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="e1ab8-389">Quando possível, formate o texto usando negrito.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-389">When possible, format the text using bold.</span></span> <span data-ttu-id="e1ab8-390">Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="e1ab8-391">Exemplo: na mensagem **deseja exibir os itens não seguros?** , clique em Sim.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

