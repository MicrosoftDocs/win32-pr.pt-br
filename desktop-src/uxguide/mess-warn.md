---
title: Mensagens de aviso
description: Uma mensagem de aviso é uma caixa de diálogo modal, mensagem in-place, notificação ou balão que alerta o usuário de uma condição que pode causar um problema no futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 42f7c669a68790ec290f931165b4aa937b5008d5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524500"
---
# <a name="warning-messages"></a><span data-ttu-id="771e6-103">Mensagens de aviso</span><span class="sxs-lookup"><span data-stu-id="771e6-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="771e6-104">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="771e6-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="771e6-105">Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)</span><span class="sxs-lookup"><span data-stu-id="771e6-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="771e6-106">Uma mensagem de aviso é uma caixa de diálogo modal, mensagem in-place, notificação ou balão que alerta o usuário de uma condição que pode causar um problema no futuro.</span><span class="sxs-lookup"><span data-stu-id="771e6-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![captura de tela de uma mensagem de aviso típica](images/mess-warn-image1.png)

<span data-ttu-id="771e6-108">Uma mensagem de aviso modal típica.</span><span class="sxs-lookup"><span data-stu-id="771e6-108">A typical modal warning message.</span></span>

<span data-ttu-id="771e6-109">A característica fundamental dos avisos é que eles envolvem o risco de perder um ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="771e6-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="771e6-110">Um ativo valioso, como dados financeiros importantes ou outros.</span><span class="sxs-lookup"><span data-stu-id="771e6-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="771e6-111">Acesso ou integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="771e6-111">System access or integrity.</span></span>
-   <span data-ttu-id="771e6-112">Privacidade ou controle sobre informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="771e6-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="771e6-113">Tempo do usuário (uma quantidade significativa, como 30 segundos ou mais).</span><span class="sxs-lookup"><span data-stu-id="771e6-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="771e6-114">Por outro lado, uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação.</span><span class="sxs-lookup"><span data-stu-id="771e6-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="771e6-115">Alguns tipos de avisos são apresentados como confirmações e, em caso afirmativos, as diretrizes de confirmação também se aplicam.</span><span class="sxs-lookup"><span data-stu-id="771e6-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="771e6-116">**Observação:** Diretrizes relacionadas a [caixas de diálogo,](win-dialog-box.md)confirmações [,](mess-confirm.md) [](mess-error.md)[ícones](vis-std-icons.md)padrão de mensagens de erro, notificações e [layout](vis-layout.md) são [apresentadas](mess-notif.md)em artigos separados.</span><span class="sxs-lookup"><span data-stu-id="771e6-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="771e6-117">Essa é a interface do usuário certa?</span><span class="sxs-lookup"><span data-stu-id="771e6-117">Is this the right user interface?</span></span>

<span data-ttu-id="771e6-118">Para decidir, considere estas perguntas:</span><span class="sxs-lookup"><span data-stu-id="771e6-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="771e6-119">**O usuário está sendo alertado de uma condição que pode causar um problema no futuro?**</span><span class="sxs-lookup"><span data-stu-id="771e6-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="771e6-120">Caso não seja, a mensagem não será um aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="771e6-121">**A interface do usuário está apresentando um erro ou um problema que já ocorreu?**</span><span class="sxs-lookup"><span data-stu-id="771e6-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="771e6-122">Em caso afirmado, use uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="771e6-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="771e6-123">**Os usuários provavelmente executarão uma ação ou alterarão seu comportamento como resultado da mensagem?**</span><span class="sxs-lookup"><span data-stu-id="771e6-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="771e6-124">Caso não seja, a condição não justifica a interrupção do usuário, portanto, é melhor suprimir o aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="771e6-125">**A condição é o resultado direto de uma ação iniciada pelo usuário?**</span><span class="sxs-lookup"><span data-stu-id="771e6-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="771e6-126">Caso não seja, considere o uso [de notificações de eventos não críticas.](mess-notif.md)</span><span class="sxs-lookup"><span data-stu-id="771e6-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="771e6-127">**A condição é uma condição especial em um controle?**</span><span class="sxs-lookup"><span data-stu-id="771e6-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="771e6-128">Em caso afirmado, use um [balão.](ctrl-balloons.md)</span><span class="sxs-lookup"><span data-stu-id="771e6-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="771e6-129">**Para confirmações, o usuário está prestes a executar uma ação arriscada?**</span><span class="sxs-lookup"><span data-stu-id="771e6-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="771e6-130">Em caso afirmativa, um aviso será apropriado se a ação tiver consequências significativas ou não puder ser facilmente desfeita.</span><span class="sxs-lookup"><span data-stu-id="771e6-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="771e6-131">**Para outros tipos de avisos, o usuário precisa agir agora ou no futuro imediato?**</span><span class="sxs-lookup"><span data-stu-id="771e6-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="771e6-132">Não exibir avisos se os usuários puderem continuar a trabalhar de forma produtiva sem problemas imediatos.</span><span class="sxs-lookup"><span data-stu-id="771e6-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="771e6-133">Adia o aviso até que a condição seja mais imediata e relevante.</span><span class="sxs-lookup"><span data-stu-id="771e6-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="771e6-134">Conceitos de design</span><span class="sxs-lookup"><span data-stu-id="771e6-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="771e6-135">Evitar o excesso de avisos</span><span class="sxs-lookup"><span data-stu-id="771e6-135">Avoid overwarning</span></span>

<span data-ttu-id="771e6-136">Estamos em excesso em programas do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="771e6-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="771e6-137">O programa típico do Windows tem avisos aparentemente em todos os lugares, aviso sobre coisas que têm pouca importância.</span><span class="sxs-lookup"><span data-stu-id="771e6-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="771e6-138">Em alguns programas, quase todas as perguntas são apresentadas como um aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="771e6-139">O excesso de avisos faz com que o uso de um programa se sinta como uma atividade perigosa e prejudica problemas realmente significativos.</span><span class="sxs-lookup"><span data-stu-id="771e6-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="771e6-140">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-140">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-141">captura de tela de uma mensagem de aviso desnecessária</span><span class="sxs-lookup"><span data-stu-id="771e6-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="771e6-142">O excesso de avisos faz com que o programa se sinta perigoso e pareça que ele foi projetado por profissionais.</span><span class="sxs-lookup"><span data-stu-id="771e6-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="771e6-143">O potencial de perda de dados ou um problema futuro sozinho é insuficiente para chamar um aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="771e6-144">Além disso, todos os resultados indesejáveis devem ser inesperados ou não intencionais e não facilmente corrigidos.</span><span class="sxs-lookup"><span data-stu-id="771e6-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="771e6-145">Caso contrário, qualquer erro do usuário pode ser interpretado para resultar em perda de dados ou em um possível problema de algum tipo e um aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="771e6-146">Características de bons avisos</span><span class="sxs-lookup"><span data-stu-id="771e6-146">Characteristics of good warnings</span></span>

<span data-ttu-id="771e6-147">Bons avisos:</span><span class="sxs-lookup"><span data-stu-id="771e6-147">Good warnings:</span></span>

-   <span data-ttu-id="771e6-148">**Envolver risco.**</span><span class="sxs-lookup"><span data-stu-id="771e6-148">**Involve risk.**</span></span> <span data-ttu-id="771e6-149">Bons avisos alertam os usuários sobre algo significativo.</span><span class="sxs-lookup"><span data-stu-id="771e6-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="771e6-150">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-150">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-151">captura de tela de 'você deseja sair?'</span><span class="sxs-lookup"><span data-stu-id="771e6-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="771e6-152">warning</span><span class="sxs-lookup"><span data-stu-id="771e6-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="771e6-153">E daí?</span><span class="sxs-lookup"><span data-stu-id="771e6-153">So what?</span></span> <span data-ttu-id="771e6-154">Essa confirmação pressu que os usuários geralmente saem de programas por acidente.</span><span class="sxs-lookup"><span data-stu-id="771e6-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="771e6-155">**Ter relevância imediata.**</span><span class="sxs-lookup"><span data-stu-id="771e6-155">**Have immediate relevance.**</span></span> <span data-ttu-id="771e6-156">Os usuários não só precisam se preocupar, mas precisam se preocupar agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="771e6-157">Normalmente, os usuários não estão interessados em problemas que possam ter mais tarde, desde que possam fazer seu trabalho agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="771e6-158">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-158">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-159">captura de tela do aviso de bateria com pouca bateria em três horas</span><span class="sxs-lookup"><span data-stu-id="771e6-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="771e6-160">Nesse caso, é melhor apenas avisar o usuário em três horas.</span><span class="sxs-lookup"><span data-stu-id="771e6-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="771e6-161">**Levar à ação.**</span><span class="sxs-lookup"><span data-stu-id="771e6-161">**Lead to action.**</span></span> <span data-ttu-id="771e6-162">Há algo que os usuários devem fazer ou estar cientes como resultado do aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="771e6-163">Talvez eles devem tomar uma ação agora ou em algum momento no futuro imediato.</span><span class="sxs-lookup"><span data-stu-id="771e6-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="771e6-164">Talvez eles executem uma tarefa de forma diferente como resultado.</span><span class="sxs-lookup"><span data-stu-id="771e6-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="771e6-165">A consequência de ignorar o aviso deve ser clara.</span><span class="sxs-lookup"><span data-stu-id="771e6-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="771e6-166">Avisos sem ações apenas fazem os usuários se sentir mal.</span><span class="sxs-lookup"><span data-stu-id="771e6-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="771e6-167">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-167">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-168">captura de tela do aviso "o live messenger está em execução"</span><span class="sxs-lookup"><span data-stu-id="771e6-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="771e6-169">Por que essa notificação é um aviso?</span><span class="sxs-lookup"><span data-stu-id="771e6-169">Why is this notification a warning?</span></span> <span data-ttu-id="771e6-170">O que os usuários devem fazer (além de se preocupar)?</span><span class="sxs-lookup"><span data-stu-id="771e6-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="771e6-171">**Não são óbvios.**</span><span class="sxs-lookup"><span data-stu-id="771e6-171">**Are not obvious.**</span></span> <span data-ttu-id="771e6-172">Não exibir um aviso para mostrar a consequência óbvia de uma ação.</span><span class="sxs-lookup"><span data-stu-id="771e6-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="771e6-173">Por exemplo, suponha que os usuários compreendam as consequências de não concluir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="771e6-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="771e6-174">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-174">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-175">captura de tela do assistente de saída? Aviso</span><span class="sxs-lookup"><span data-stu-id="771e6-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="771e6-176">Cancelar um assistente incompleto significa que a tarefa não é realizada... quem sabia?</span><span class="sxs-lookup"><span data-stu-id="771e6-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="771e6-177">**Ocorrem raramente.**</span><span class="sxs-lookup"><span data-stu-id="771e6-177">**Occur infrequently.**</span></span> <span data-ttu-id="771e6-178">Avisos constantes tornam-se rapidamente ineficaz e entediantes.</span><span class="sxs-lookup"><span data-stu-id="771e6-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="771e6-179">Os usuários geralmente se concentram mais em se desfazer do aviso do que resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="771e6-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="771e6-180">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-180">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-181">captura de tela do aviso 'atualizar assinaturas de vírus'</span><span class="sxs-lookup"><span data-stu-id="771e6-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="771e6-182">É mais provável que os usuários se concentrem em se desfazer do aviso do que corrigir o problema subjacente.</span><span class="sxs-lookup"><span data-stu-id="771e6-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="771e6-183">Uma mensagem que não tem essas características ainda pode ser uma boa mensagem, mas não um bom aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="771e6-184">Determinar o tipo de mensagem apropriado</span><span class="sxs-lookup"><span data-stu-id="771e6-184">Determine the appropriate message type</span></span>

<span data-ttu-id="771e6-185">Alguns problemas podem ser apresentados como um erro, aviso ou informações, dependendo da ênfase e frase.</span><span class="sxs-lookup"><span data-stu-id="771e6-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="771e6-186">Por exemplo, suponha que uma página da Web não possa carregar um controle ActiveX não assinado com base na configuração atual do Windows Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="771e6-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="771e6-187">**Erro.**</span><span class="sxs-lookup"><span data-stu-id="771e6-187">**Error.**</span></span> <span data-ttu-id="771e6-188">"Esta página não pode carregar um controle ActiveX não assinado."</span><span class="sxs-lookup"><span data-stu-id="771e6-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="771e6-189">(Formulado como um problema existente.)</span><span class="sxs-lookup"><span data-stu-id="771e6-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="771e6-190">**Aviso.**</span><span class="sxs-lookup"><span data-stu-id="771e6-190">**Warning.**</span></span> <span data-ttu-id="771e6-191">"Esta página pode não se comportar conforme o esperado porque o Windows Internet Explorer não está configurado para carregar controles ActiveX não assinados."</span><span class="sxs-lookup"><span data-stu-id="771e6-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="771e6-192">ou "Permitir que esta página instale um controle ActiveX não assinado?</span><span class="sxs-lookup"><span data-stu-id="771e6-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="771e6-193">Fazer isso de fontes não confiáveis pode prejudicar o computador."</span><span class="sxs-lookup"><span data-stu-id="771e6-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="771e6-194">(Ambos frases como condições que podem causar problemas futuros.)</span><span class="sxs-lookup"><span data-stu-id="771e6-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="771e6-195">**Informações.**</span><span class="sxs-lookup"><span data-stu-id="771e6-195">**Information.**</span></span> <span data-ttu-id="771e6-196">"Você configurou o Windows Internet Explorer para bloquear controles ActiveX não assinados."</span><span class="sxs-lookup"><span data-stu-id="771e6-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="771e6-197">(Formulado como uma instrução de fato.)</span><span class="sxs-lookup"><span data-stu-id="771e6-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="771e6-198">**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.**</span><span class="sxs-lookup"><span data-stu-id="771e6-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="771e6-199">Normalmente, se um problema bloquear o andamento do usuário, você deverá apresentá-lo como um erro; se o usuário puder continuar, apresente-o como um aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="771e6-200">Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e escolha um ícone[(padrão](vis-std-icons.md) ou não) que corresponda ao texto.</span><span class="sxs-lookup"><span data-stu-id="771e6-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="771e6-201">O texto de instrução principal e os ícones devem sempre corresponder.</span><span class="sxs-lookup"><span data-stu-id="771e6-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="771e6-202">Ser específico</span><span class="sxs-lookup"><span data-stu-id="771e6-202">Be specific</span></span>

<span data-ttu-id="771e6-203">Os avisos são mais atraentes quando as seguintes informações são específicas e claras:</span><span class="sxs-lookup"><span data-stu-id="771e6-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="771e6-204">A origem do aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-204">The source of the warning.</span></span>
-   <span data-ttu-id="771e6-205">A condição específica e o possível problema.</span><span class="sxs-lookup"><span data-stu-id="771e6-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="771e6-206">O que o usuário deve fazer sobre isso.</span><span class="sxs-lookup"><span data-stu-id="771e6-206">What the user should do about it.</span></span>
-   <span data-ttu-id="771e6-207">O que acontece se o usuário não fizer nada.</span><span class="sxs-lookup"><span data-stu-id="771e6-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="771e6-208">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-208">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-209">captura de tela de aviso de alerta de risco significativo</span><span class="sxs-lookup"><span data-stu-id="771e6-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="771e6-210">Neste exemplo, qual é o problema potencial?</span><span class="sxs-lookup"><span data-stu-id="771e6-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="771e6-211">O que o usuário deve fazer, além de não usar o projetor pela rede?</span><span class="sxs-lookup"><span data-stu-id="771e6-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="771e6-212">Sem informações mais específicas, tudo o que o usuário pode fazer é se sentir mal em continuar.</span><span class="sxs-lookup"><span data-stu-id="771e6-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="771e6-213">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-213">**Correct:**</span></span>

![<span data-ttu-id="771e6-214">captura de tela do aviso de problema e consequências</span><span class="sxs-lookup"><span data-stu-id="771e6-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="771e6-215">Neste exemplo, o problema e as consequências são claros.</span><span class="sxs-lookup"><span data-stu-id="771e6-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="771e6-216">Às vezes, há um problema potencial legítimo que se deve informar aos usuários sobre, mas a solução e as consequências não são conhecidas com certeza.</span><span class="sxs-lookup"><span data-stu-id="771e6-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="771e6-217">Em vez de dar um aviso vaga, seja específico, dando as informações mais prováveis ou o exemplo mais comum.</span><span class="sxs-lookup"><span data-stu-id="771e6-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="771e6-218">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-218">**Correct:**</span></span>

![<span data-ttu-id="771e6-219">captura de tela do aviso de erro de rede e soluções</span><span class="sxs-lookup"><span data-stu-id="771e6-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="771e6-220">Neste exemplo, o aviso é específico fornecendo a solução mais provável.</span><span class="sxs-lookup"><span data-stu-id="771e6-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="771e6-221">No entanto, nesses casos, use palavras que indicam que há outras possibilidades.</span><span class="sxs-lookup"><span data-stu-id="771e6-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="771e6-222">Caso contrário, os usuários poderão ser mal-sinal.</span><span class="sxs-lookup"><span data-stu-id="771e6-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="771e6-223">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-223">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-224">captura de tela do aviso de cabo de rede desconectado</span><span class="sxs-lookup"><span data-stu-id="771e6-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="771e6-225">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-225">**Correct:**</span></span>

![<span data-ttu-id="771e6-226">captura de tela do cabo pode ser um aviso desconectado</span><span class="sxs-lookup"><span data-stu-id="771e6-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="771e6-227">No exemplo incorreto, os usuários serão confundidos se o cabo estiver claramente conectado.</span><span class="sxs-lookup"><span data-stu-id="771e6-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="771e6-228">**Se você fizer apenas duas coisas...**</span><span class="sxs-lookup"><span data-stu-id="771e6-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="771e6-229">Não se preocupe.</span><span class="sxs-lookup"><span data-stu-id="771e6-229">Don't overwarn.</span></span> <span data-ttu-id="771e6-230">Limite avisos a condições que envolvem risco e são imediatamente relevantes, ativas, não óbvias e pouco frequentes.</span><span class="sxs-lookup"><span data-stu-id="771e6-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="771e6-231">Caso contrário, remova ou refrase a mensagem.</span><span class="sxs-lookup"><span data-stu-id="771e6-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="771e6-232">Forneça informações específicas e úteis.</span><span class="sxs-lookup"><span data-stu-id="771e6-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="771e6-233">Padrões de uso</span><span class="sxs-lookup"><span data-stu-id="771e6-233">Usage patterns</span></span>

<span data-ttu-id="771e6-234">Os avisos têm vários padrões de uso:</span><span class="sxs-lookup"><span data-stu-id="771e6-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="771e6-235"><strong>Reconhecimento</strong></span><span class="sxs-lookup"><span data-stu-id="771e6-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="771e6-236">Tornar o usuário ciente de uma condição ou possível problema, mas o usuário pode não ter que fazer nada agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="771e6-237">Exemplos de avisos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="771e6-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="771e6-238">Os avisos de reconhecimento têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="771e6-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="771e6-239"><strong>Instrução principal:</strong> Descreva a condição ou o possível problema.</span><span class="sxs-lookup"><span data-stu-id="771e6-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="771e6-240"><strong>Instrução complementar:</strong> Explique a implicação e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="771e6-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="771e6-241"><strong>Botões de commit:</strong> Perto.</span><span class="sxs-lookup"><span data-stu-id="771e6-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="771e6-242"><strong>Prevenção de erros</strong></span><span class="sxs-lookup"><span data-stu-id="771e6-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="771e6-243">Tornar o usuário ciente das informações que podem impedir um problema, especialmente ao fazer escolhas.</span><span class="sxs-lookup"><span data-stu-id="771e6-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="771e6-244">Os avisos de prevenção de erros são apresentados melhor usando um ícone de aviso in-locar e um texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="771e6-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="771e6-245">Exemplos de avisos de prevenção de erros.</span><span class="sxs-lookup"><span data-stu-id="771e6-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="771e6-246"><strong>Problema iminente</strong></span><span class="sxs-lookup"><span data-stu-id="771e6-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="771e6-247">O usuário precisa fazer algo agora para evitar um problema iminente.</span><span class="sxs-lookup"><span data-stu-id="771e6-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="771e6-248">Um exemplo de um aviso de problema iminente.</span><span class="sxs-lookup"><span data-stu-id="771e6-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="771e6-249">Os avisos de problema iminente têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="771e6-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="771e6-250"><strong>Instrução principal:</strong> Descrever o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="771e6-251"><strong>Instrução complementar:</strong> Explique a condição e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="771e6-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="771e6-252"><strong>Botões de commit:</strong> Um botão de comando ou um link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="771e6-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="771e6-253"><strong>Confirmação de ação arriscada</strong></span><span class="sxs-lookup"><span data-stu-id="771e6-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="771e6-254">Confirme se o usuário deseja prosseguir com uma ação que tem algum risco e não pode ser facilmente desfeita.</span><span class="sxs-lookup"><span data-stu-id="771e6-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="771e6-255">Um exemplo de confirmação de ação arriscada.</span><span class="sxs-lookup"><span data-stu-id="771e6-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="771e6-256">As confirmações de ação arriscada têm a seguinte apresentação:</span><span class="sxs-lookup"><span data-stu-id="771e6-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="771e6-257"><strong>Instrução principal:</strong> Faça uma pergunta para determinar se o usuário deseja continuar.</span><span class="sxs-lookup"><span data-stu-id="771e6-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="771e6-258"><strong>Instrução complementar:</strong> Explique os motivos não óbvios pelos quais o usuário talvez não queira continuar.</span><span class="sxs-lookup"><span data-stu-id="771e6-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="771e6-259"><strong>Botões de commit:</strong> Sim, não.</span><span class="sxs-lookup"><span data-stu-id="771e6-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="771e6-260">Para ver diretrizes sobre esse padrão, consulte <a href="mess-confirm.md">Confirmações</a>.</span><span class="sxs-lookup"><span data-stu-id="771e6-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="771e6-261">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="771e6-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="771e6-262">Apresentação</span><span class="sxs-lookup"><span data-stu-id="771e6-262">Presentation</span></span>

-   <span data-ttu-id="771e6-263">**Escolha a interface do usuário de apresentação com base no tipo de informação:**</span><span class="sxs-lookup"><span data-stu-id="771e6-263">**Choose the presentation UI based on the type of information:**</span></span>



| <span data-ttu-id="771e6-264">Interface do usuário</span><span class="sxs-lookup"><span data-stu-id="771e6-264">User interface</span></span>  | <span data-ttu-id="771e6-265">Melhor usado para</span><span class="sxs-lookup"><span data-stu-id="771e6-265">Best used for</span></span> |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771e6-266">Caixas de diálogo modais</span><span class="sxs-lookup"><span data-stu-id="771e6-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="771e6-267">Avisos críticos (incluindo confirmações) aos quais os usuários devem responder agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="771e6-268">In-place</span><span class="sxs-lookup"><span data-stu-id="771e6-268">In-place</span></span><br/>           | <span data-ttu-id="771e6-269">Informações que podem impedir um problema, especialmente quando os usuários estão fazendo escolhas.</span><span class="sxs-lookup"><span data-stu-id="771e6-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="771e6-270">Banners</span><span class="sxs-lookup"><span data-stu-id="771e6-270">Banners</span></span><br/>            | <span data-ttu-id="771e6-271">Informações que podem impedir um problema, especialmente quando relacionadas à conclusão de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="771e6-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="771e6-272">Notificações</span><span class="sxs-lookup"><span data-stu-id="771e6-272">Notifications</span></span><br/>      | <span data-ttu-id="771e6-273">Eventos significativos ou status que podem ser ignorados com segurança, pelo menos temporariamente.</span><span class="sxs-lookup"><span data-stu-id="771e6-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="771e6-274">Balões</span><span class="sxs-lookup"><span data-stu-id="771e6-274">Balloons</span></span><br/>           | <span data-ttu-id="771e6-275">Um controle está em um estado que afeta a entrada.</span><span class="sxs-lookup"><span data-stu-id="771e6-275">A control is in a state that affects input.</span></span> <span data-ttu-id="771e6-276">Esse estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada.</span><span class="sxs-lookup"><span data-stu-id="771e6-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="771e6-277">**Para caixas de diálogo modais:**</span><span class="sxs-lookup"><span data-stu-id="771e6-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="771e6-278">**Use caixas de diálogo de tarefa sempre que apropriado para obter uma aparência e layout consistentes.**</span><span class="sxs-lookup"><span data-stu-id="771e6-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="771e6-279">As caixas de diálogo de tarefa exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="771e6-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="771e6-280">**Exibe apenas uma mensagem de aviso por condição.**</span><span class="sxs-lookup"><span data-stu-id="771e6-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="771e6-281">Por exemplo, exibe um único aviso que explica completamente uma condição em vez de descrevê-la um detalhe por vez por mensagem.</span><span class="sxs-lookup"><span data-stu-id="771e6-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="771e6-282">Exibir uma sequência de caixas de diálogo de aviso para uma única condição é confuso e entediante.</span><span class="sxs-lookup"><span data-stu-id="771e6-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="771e6-283">**Não exibir um aviso mais de uma vez por condição.**</span><span class="sxs-lookup"><span data-stu-id="771e6-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="771e6-284">Avisos constantes tornam-se rapidamente ineficaz e entediantes.</span><span class="sxs-lookup"><span data-stu-id="771e6-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="771e6-285">Os usuários geralmente se concentram mais em se desfazer do aviso do que resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="771e6-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="771e6-286">Se você tiver que avisar repetidamente para uma única condição, use [o escalonamento progressivo](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="771e6-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="771e6-287">**Não acompanhe avisos com um efeito de som ou um aviso.**</span><span class="sxs-lookup"><span data-stu-id="771e6-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="771e6-288">Fazer isso é jarring e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="771e6-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="771e6-289">**Exceção:** Se o usuário precisa responder imediatamente, você pode usar um efeito de som.</span><span class="sxs-lookup"><span data-stu-id="771e6-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="771e6-290">Ícones</span><span class="sxs-lookup"><span data-stu-id="771e6-290">Icons</span></span>

-   <span data-ttu-id="771e6-291">Não coloque um ícone de aviso na barra de título de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="771e6-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="771e6-292">**Use um ícone de aviso.**</span><span class="sxs-lookup"><span data-stu-id="771e6-292">**Use a warning icon.**</span></span> <span data-ttu-id="771e6-293">Exceções:</span><span class="sxs-lookup"><span data-stu-id="771e6-293">Exceptions:</span></span>
    -   <span data-ttu-id="771e6-294">Se o aviso for para um recurso que tenha um ícone, você poderá usar o ícone de recurso com uma sobreposição de aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="771e6-295">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-295">**Correct:**</span></span>

        ![<span data-ttu-id="771e6-296">captura de tela do ícone de bloqueio com sobreposição do ícone de aviso</span><span class="sxs-lookup"><span data-stu-id="771e6-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="771e6-297">Neste exemplo, o ícone de recurso tem uma sobreposição de aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="771e6-298">Para caixas de diálogo modais com uma nota de rodapé de aviso, coloque o ícone de aviso na nota de rodapé em vez da área de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="771e6-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="771e6-299">**Correto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-299">**Correct:**</span></span>

    ![<span data-ttu-id="771e6-300">captura de tela do ícone de aviso na nota de rodapé da caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="771e6-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="771e6-301">Neste exemplo, a nota de rodapé tem o ícone de aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="771e6-302">Para obter mais diretrizes e exemplos, consulte [ícones padrão](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="771e6-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="771e6-303">Não mostrar esta mensagem novamente</span><span class="sxs-lookup"><span data-stu-id="771e6-303">Don't show this message again</span></span>

-   <span data-ttu-id="771e6-304">**Se uma caixa de diálogo de aviso precisar dessa opção, reconsidere o aviso e sua frequência.**</span><span class="sxs-lookup"><span data-stu-id="771e6-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="771e6-305">Se ele tem todas as características de um bom aviso (envolve risco e é imediatamente relevante, acionável, não óbvio e incomum), não deve fazer sentido para os usuários suprimirem.</span><span class="sxs-lookup"><span data-stu-id="771e6-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="771e6-306">Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="771e6-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="771e6-307">Divulgação progressiva</span><span class="sxs-lookup"><span data-stu-id="771e6-307">Progressive disclosure</span></span>

-   <span data-ttu-id="771e6-308">**Se você precisar incluir informações avançadas em uma mensagem de aviso, revele-as usando botões de divulgação progressiva** (por exemplo, "mostrar detalhes").</span><span class="sxs-lookup"><span data-stu-id="771e6-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="771e6-309">Fazer isso simplifica o aviso para uso típico.</span><span class="sxs-lookup"><span data-stu-id="771e6-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="771e6-310">Não oculte as informações necessárias porque os usuários talvez não as encontrem.</span><span class="sxs-lookup"><span data-stu-id="771e6-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="771e6-311">**Não use "mostrar detalhes", a menos que realmente haja mais detalhes.**</span><span class="sxs-lookup"><span data-stu-id="771e6-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="771e6-312">Não apenas redeclare as informações existentes em um formato diferente.</span><span class="sxs-lookup"><span data-stu-id="771e6-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="771e6-313">Para obter diretrizes de rotulamento, consulte [divulgação progressiva](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="771e6-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="771e6-314">Valores padrão</span><span class="sxs-lookup"><span data-stu-id="771e6-314">Default values</span></span>

-   <span data-ttu-id="771e6-315">**Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.**</span><span class="sxs-lookup"><span data-stu-id="771e6-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="771e6-316">Text</span><span class="sxs-lookup"><span data-stu-id="771e6-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="771e6-317">Geral</span><span class="sxs-lookup"><span data-stu-id="771e6-317">General</span></span>

-   <span data-ttu-id="771e6-318">**Remova o texto redundante.**</span><span class="sxs-lookup"><span data-stu-id="771e6-318">**Remove redundant text.**</span></span> <span data-ttu-id="771e6-319">Procure por ele em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação.</span><span class="sxs-lookup"><span data-stu-id="771e6-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="771e6-320">Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.</span><span class="sxs-lookup"><span data-stu-id="771e6-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="771e6-321">**Não use os termos "aviso" ou "cuidado" no texto.**</span><span class="sxs-lookup"><span data-stu-id="771e6-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="771e6-322">Quando [usado corretamente](vis-std-icons.md), o ícone de aviso comunica suficientemente que os usuários devem continuar com cautela.</span><span class="sxs-lookup"><span data-stu-id="771e6-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="771e6-323">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-323">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-324">captura de tela de uso desnecessário de aviso no texto</span><span class="sxs-lookup"><span data-stu-id="771e6-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="771e6-325">Neste exemplo, o termo "aviso" é desnecessário.</span><span class="sxs-lookup"><span data-stu-id="771e6-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="771e6-326">Títulos</span><span class="sxs-lookup"><span data-stu-id="771e6-326">Titles</span></span>

-   <span data-ttu-id="771e6-327">**Use o título para identificar o comando ou recurso do qual o aviso veio.**</span><span class="sxs-lookup"><span data-stu-id="771e6-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="771e6-328">Exceções:</span><span class="sxs-lookup"><span data-stu-id="771e6-328">Exceptions:</span></span>
    -   <span data-ttu-id="771e6-329">Se um aviso for exibido por vários comandos diferentes, considere usar o nome do programa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="771e6-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="771e6-330">Se esse título fosse redundante ou confuso com a instrução principal, use o nome do programa em vez disso.</span><span class="sxs-lookup"><span data-stu-id="771e6-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="771e6-331">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-331">**Incorrect:**</span></span>

![<span data-ttu-id="771e6-332">captura de tela do título da caixa de diálogo de aviso de segurança</span><span class="sxs-lookup"><span data-stu-id="771e6-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="771e6-333">Neste exemplo, "aviso de segurança" não identifica o comando ou o recurso do qual veio o aviso.</span><span class="sxs-lookup"><span data-stu-id="771e6-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="771e6-334">**Não use o título para explicar o que fazer na caixa de diálogo** que é a finalidade da instrução principal.</span><span class="sxs-lookup"><span data-stu-id="771e6-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="771e6-335">Use [maiúsculas e minúsculas no estilo de título](glossary.md), sem pontuação final.</span><span class="sxs-lookup"><span data-stu-id="771e6-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="771e6-336">Instruções principais</span><span class="sxs-lookup"><span data-stu-id="771e6-336">Main instructions</span></span>

-   <span data-ttu-id="771e6-337">A instrução principal para um aviso se baseia em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="771e6-337">The main instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="771e6-338">Padrão</span><span class="sxs-lookup"><span data-stu-id="771e6-338">Pattern</span></span>                        | <span data-ttu-id="771e6-339">Instrução principal</span><span class="sxs-lookup"><span data-stu-id="771e6-339">Main instruction</span></span>                                               |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="771e6-340">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="771e6-340">Awareness</span></span><br/>                 | <span data-ttu-id="771e6-341">Descreva a condição ou o problema potencial.</span><span class="sxs-lookup"><span data-stu-id="771e6-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="771e6-342">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="771e6-342">Imminent problem</span></span><br/>          | <span data-ttu-id="771e6-343">Descreva o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="771e6-344">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="771e6-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="771e6-345">Faça uma pergunta para determinar se o usuário deseja continuar.</span><span class="sxs-lookup"><span data-stu-id="771e6-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="771e6-346">captura de tela de uma notificação de bateria fraca</span><span class="sxs-lookup"><span data-stu-id="771e6-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="771e6-347">Neste exemplo, a notificação de bateria fraca é um aviso de conscientização, portanto, a instrução principal descreve a condição.</span><span class="sxs-lookup"><span data-stu-id="771e6-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="771e6-348">captura de tela de alterar a bateria imediatamente aviso</span><span class="sxs-lookup"><span data-stu-id="771e6-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="771e6-349">Neste exemplo, a caixa de diálogo de bateria fraca é um problema iminente, portanto, a instrução principal descreve o que o usuário precisa fazer agora.</span><span class="sxs-lookup"><span data-stu-id="771e6-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="771e6-350">**Seja conciso Use apenas uma única frase completa.**</span><span class="sxs-lookup"><span data-stu-id="771e6-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="771e6-351">Remova a instrução principal para as informações essenciais.</span><span class="sxs-lookup"><span data-stu-id="771e6-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="771e6-352">Se você precisar explicar algo mais, use uma instrução complementar.</span><span class="sxs-lookup"><span data-stu-id="771e6-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="771e6-353">**Use palavras como "Now" e "imediatamente" se o usuário precisar agir imediatamente.**</span><span class="sxs-lookup"><span data-stu-id="771e6-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="771e6-354">Não use essas palavras se não houver urgência.</span><span class="sxs-lookup"><span data-stu-id="771e6-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="771e6-355">**Seja específico se houver objetos envolvidos, forneça seus nomes completos.**</span><span class="sxs-lookup"><span data-stu-id="771e6-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="771e6-356">Use [a capitalização no estilo de frase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="771e6-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="771e6-357">Instruções complementares</span><span class="sxs-lookup"><span data-stu-id="771e6-357">Supplemental instructions</span></span>

-   <span data-ttu-id="771e6-358">A instrução complementar para um aviso se baseia em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="771e6-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="771e6-359">Padrão</span><span class="sxs-lookup"><span data-stu-id="771e6-359">Pattern</span></span>            | <span data-ttu-id="771e6-360">Instrução complementar</span><span class="sxs-lookup"><span data-stu-id="771e6-360">Supplemental instruction</span></span>                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="771e6-361">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="771e6-361">Awareness</span></span><br/>                 | <span data-ttu-id="771e6-362">Explique a implicação e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="771e6-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="771e6-363">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="771e6-363">Imminent problem</span></span><br/>          | <span data-ttu-id="771e6-364">Explique a condição e por que ela é importante.</span><span class="sxs-lookup"><span data-stu-id="771e6-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="771e6-365">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="771e6-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="771e6-366">Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar.</span><span class="sxs-lookup"><span data-stu-id="771e6-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="771e6-367">**Não repita a instrução principal com uma palavra ligeiramente diferente.**</span><span class="sxs-lookup"><span data-stu-id="771e6-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="771e6-368">Em vez disso, omita a instrução complementar se não houver mais a adicionar.</span><span class="sxs-lookup"><span data-stu-id="771e6-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="771e6-369">Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.</span><span class="sxs-lookup"><span data-stu-id="771e6-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="771e6-370">Botões de confirmação</span><span class="sxs-lookup"><span data-stu-id="771e6-370">Commit buttons</span></span>

-   <span data-ttu-id="771e6-371">Para caixas de diálogo de aviso, os botões de confirmação se baseiam em seu padrão de design:</span><span class="sxs-lookup"><span data-stu-id="771e6-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



| <span data-ttu-id="771e6-372">Padrão</span><span class="sxs-lookup"><span data-stu-id="771e6-372">Pattern</span></span>               | <span data-ttu-id="771e6-373">Botões de confirmação</span><span class="sxs-lookup"><span data-stu-id="771e6-373">Commit buttons</span></span>        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771e6-374">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="771e6-374">Awareness</span></span><br/>                 | <span data-ttu-id="771e6-375">Fechar.</span><span class="sxs-lookup"><span data-stu-id="771e6-375">Close.</span></span> <span data-ttu-id="771e6-376">Não use OK porque ele sugere que problemas potenciais estão OK.</span><span class="sxs-lookup"><span data-stu-id="771e6-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="771e6-377">Problema iminente</span><span class="sxs-lookup"><span data-stu-id="771e6-377">Imminent problem</span></span><br/>          | <span data-ttu-id="771e6-378">Um botão de comando ou link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="771e6-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="771e6-379">Confirmação de ação arriscada</span><span class="sxs-lookup"><span data-stu-id="771e6-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="771e6-380">Sim, não.</span><span class="sxs-lookup"><span data-stu-id="771e6-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="771e6-381">**Incorreto:**</span><span class="sxs-lookup"><span data-stu-id="771e6-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="771e6-382">captura de tela da caixa de diálogo de aviso com o botão OK</span><span class="sxs-lookup"><span data-stu-id="771e6-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="771e6-383">Os problemas não estão OK, portanto, use fechar.</span><span class="sxs-lookup"><span data-stu-id="771e6-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="771e6-384">Documentação</span><span class="sxs-lookup"><span data-stu-id="771e6-384">Documentation</span></span>

<span data-ttu-id="771e6-385">Ao fazer referência a avisos:</span><span class="sxs-lookup"><span data-stu-id="771e6-385">When referring to warnings:</span></span>

-   <span data-ttu-id="771e6-386">Se o aviso faz uma pergunta, consulte um aviso por sua pergunta; caso contrário, use a instrução principal.</span><span class="sxs-lookup"><span data-stu-id="771e6-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="771e6-387">Se a pergunta ou a instrução principal for longa ou detalhada, resuma-a.</span><span class="sxs-lookup"><span data-stu-id="771e6-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="771e6-388">Se necessário, você pode se referir a uma caixa de diálogo de aviso como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="771e6-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="771e6-389">Quando possível, formate o texto usando negrito.</span><span class="sxs-lookup"><span data-stu-id="771e6-389">When possible, format the text using bold.</span></span> <span data-ttu-id="771e6-390">Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.</span><span class="sxs-lookup"><span data-stu-id="771e6-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="771e6-391">Exemplo: na mensagem **deseja exibir os itens não seguros?** , clique em Sim.</span><span class="sxs-lookup"><span data-stu-id="771e6-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

