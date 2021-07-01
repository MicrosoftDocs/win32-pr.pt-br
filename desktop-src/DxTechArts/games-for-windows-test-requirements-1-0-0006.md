---
title: Melhores práticas para casos de teste dos jogos para Windows no Windows XP, Windows Vista, Windows 7 e Windows 8
description: Este artigo fornece casos de teste para jogos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120271"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="c0c27-103">Jogos para casos de teste do Windows: práticas recomendadas para jogos no Windows XP, Windows Vista, Windows 7 e Windows 8</span><span class="sxs-lookup"><span data-stu-id="c0c27-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="c0c27-104">Este artigo fornece casos de teste para jogos para Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="c0c27-105">Como usar esse artigo?</span><span class="sxs-lookup"><span data-stu-id="c0c27-105">How to Use This Article</span></span>

<span data-ttu-id="c0c27-106">Há três seções principais para este artigo:</span><span class="sxs-lookup"><span data-stu-id="c0c27-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="c0c27-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de teste**</span><span class="sxs-lookup"><span data-stu-id="c0c27-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-108">Cada requisito de teste neste documento tem quatro seções principais: um título e uma tabela com três seções notáveis (coluna esquerda, direita superior, direita inferior).</span><span class="sxs-lookup"><span data-stu-id="c0c27-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="c0c27-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título</span><span class="sxs-lookup"><span data-stu-id="c0c27-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-110">Nome do caso de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Caixa, coluna da extrema esquerda</span><span class="sxs-lookup"><span data-stu-id="c0c27-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-112">Nomes dos sistemas operacionais aos quais se aplica o caso de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, direita superior</span><span class="sxs-lookup"><span data-stu-id="c0c27-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-114">Breve resumo do caso de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, direita inferior</span><span class="sxs-lookup"><span data-stu-id="c0c27-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-116">Detalhes do caso de teste real.</span><span class="sxs-lookup"><span data-stu-id="c0c27-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0c27-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Exemplo de script de teste**</span><span class="sxs-lookup"><span data-stu-id="c0c27-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-118">Esta seção é um exemplo da sequência que uma etapa de teste típica seguiria se estiver usando os requisitos de teste como um guia.</span><span class="sxs-lookup"><span data-stu-id="c0c27-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas da ferramenta de teste**</span><span class="sxs-lookup"><span data-stu-id="c0c27-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-120">Esta seção contém observações detalhadas sobre cada uma das ferramentas de teste usadas para verificar condições de aprovação ou falha nos requisitos de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="c0c27-121">Requisitos de teste</span><span class="sxs-lookup"><span data-stu-id="c0c27-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="c0c27-122">1. requisitos do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="c0c27-123">1,1 explorador de jogos do Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-124">Windows 7</span></span><br/> <span data-ttu-id="c0c27-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-126">O jogo deve estar visível no explorador de jogos no Windows Vista e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0c27-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="c0c27-127">Quando selecionado, o jogo também deve exibir metadados corretos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="c0c27-128">A instalação não deve criar um atalho para iniciar o jogo na área de trabalho, no menu iniciar ou em qualquer outro local.</span><span class="sxs-lookup"><span data-stu-id="c0c27-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="c0c27-129">Tarefas e atalhos para remoção não devem ser criados.</span><span class="sxs-lookup"><span data-stu-id="c0c27-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-130">Depois de instalar o jogo, abra o explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="c0c27-131">Verifique se o ícone de jogo é exibido no explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="c0c27-132">Clique com o botão direito do mouse no ícone e teste a & tarefa de suporte de reprodução definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="c0c27-133">Clique no ícone e verifique se os metadados (Publicador, desenvolvedor, gênero, data de lançamento, versão) na parte inferior são exibidos e estão corretos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="c0c27-134">Verifique se o ícone de jogo exibe informações do WEI (índice de experiência do Windows) no explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="c0c27-135">Verifique se os hiperlinks de jogos para os metadados funcionam corretamente no explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="c0c27-136">(Se os hiperlinks não aparecerem, esse é um sinal possível para o qual o exe não está assinado; consulte a <a href="#23-sign-files">seção 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="c0c27-137">Verifique se o jogo exibe classificação de controle dos pais preciso no explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="c0c27-138">(Se estiver sem classificação, verifique se esse é um jogo sem classificação; caso contrário, esse é um indicador de que o exe não está assinado; consulte a <a href="#23-sign-files">seção 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="c0c27-139">Verifique se o jogo não coloca os atalhos de inicialização na área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="c0c27-140">Clique em Iniciar-> todos os programas.</span><span class="sxs-lookup"><span data-stu-id="c0c27-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="c0c27-141">Verifique se o jogo não coloca os atalhos de inicialização no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="c0c27-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="c0c27-142">Verifique se o jogo não coloca os atalhos de desinstalação no menu iniciar fora do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c0c27-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="c0c27-143">Se o jogo for distribuído digitalmente, verifique se o provedor de serviços aparece no explorador de jogos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="c0c27-144">1,2 controles de segurança/pais da família Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-145">Windows 7</span></span><br/> <span data-ttu-id="c0c27-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-147">O jogo deve ser executado dentro do contexto de um &quot; usuário padrão &quot; .</span><span class="sxs-lookup"><span data-stu-id="c0c27-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="c0c27-148">Os controles dos pais devem ser capazes de bloquear o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="c0c27-149">Verifique se o GDF tem nomes EXE.</span><span class="sxs-lookup"><span data-stu-id="c0c27-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-150">Crie uma conta de usuário padrão no Windows Vista ou no Windows 7 chamada Toby.</span><span class="sxs-lookup"><span data-stu-id="c0c27-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="c0c27-151">Iniciar-> painel de controle-> adicionar ou remover contas de usuário-> criar nova conta</span><span class="sxs-lookup"><span data-stu-id="c0c27-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="c0c27-152">Como Jane, da conta de administrador, configure os controles dos pais para o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="c0c27-153">Iniciar-> painel de controle-> configurar controles dos pais para qualquer usuário-> Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="c0c27-154">Verifique se o jogo é iniciado no ícone do explorador de jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="c0c27-155">Verifique se o jogo exibe a classificação de controle dos pais preciso abaixo do título do jogo no painel de controle dos controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="c0c27-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="c0c27-156">Antes de aplicar os controles dos pais, verifique se o jogo não solicita as credenciais de administrador na inicialização.</span><span class="sxs-lookup"><span data-stu-id="c0c27-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="c0c27-157">Defina controles dos pais como &quot; ativado &quot; .</span><span class="sxs-lookup"><span data-stu-id="c0c27-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="c0c27-158">Na seção Configurações do Windows, clique em jogos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="c0c27-159">Clique em OK (agora, a configuração deve ser ao seu com &quot; /todos os jogos &quot; ).</span><span class="sxs-lookup"><span data-stu-id="c0c27-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="c0c27-160">Verifique se o jogo é executado com essas configurações como o usuário Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="c0c27-161">Faça logoff como Jane e faça logon como Toby.</span><span class="sxs-lookup"><span data-stu-id="c0c27-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="c0c27-162">Verifique se o jogo é executado com essas configurações como usuário Toby.</span><span class="sxs-lookup"><span data-stu-id="c0c27-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="c0c27-163">Faça logoff como Toby e faça logon como Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="c0c27-164">Volte para a tela anterior e selecione &quot; definir classificações de &quot; jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="c0c27-165">Selecione uma classificação inferior à classificação de ESRB do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-166">Se o jogo não for classificado, ignore esta etapa e vá para a próxima parte deste teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="c0c27-167">Pode ser necessário escolher um sistema de classificação diferente para encontrar uma classificação de jogo, dependendo da localidade do idioma do SKU que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="c0c27-168">Faça logoff como Jane e faça logon como Toby.</span><span class="sxs-lookup"><span data-stu-id="c0c27-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="c0c27-169">Verifique se o jogo não é iniciado para o usuário Toby quando ESRB está bloqueado pelo usuário Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="c0c27-170">Faça logoff como Toby e faça logon como Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="c0c27-171">Se alterado anteriormente, restaure as configurações de ESRB.</span><span class="sxs-lookup"><span data-stu-id="c0c27-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="c0c27-172">Se não houver configurações de ESRB, selecione &quot; bloquear ou permitir jogos específicos &quot; e selecione o jogo por nome.</span><span class="sxs-lookup"><span data-stu-id="c0c27-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="c0c27-173">Faça logoff como Jane e faça logon como Toby.</span><span class="sxs-lookup"><span data-stu-id="c0c27-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="c0c27-174">Verifique se o jogo não é iniciado para o usuário Toby quando o EXE/Name é bloqueado pelo usuário Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="c0c27-175">Faça logoff como Toby e volte como Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="c0c27-176">Como Jane, abra controles de usuário-> restrições de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="c0c27-177">Clique em &quot; Toby só pode usar os programas permitidos &quot; e clicar em OK (ou seja, não permitir nenhum EXEs).</span><span class="sxs-lookup"><span data-stu-id="c0c27-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="c0c27-178">Ir para controles de usuário | Os jogos controlam e permitem o jogo específico usando a classificação ESRB.</span><span class="sxs-lookup"><span data-stu-id="c0c27-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="c0c27-179">Faça logoff como Jane e faça logon como Toby e tente jogar o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="c0c27-180">Verifique se o jogo não está bloqueado e se o Toby pode reproduzi-lo quando &quot; não permitir que nenhum EXEs &quot; esteja definido.</span><span class="sxs-lookup"><span data-stu-id="c0c27-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="c0c27-181">1,3 jogos sofisticados salvos no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="c0c27-182">Esse requisito foi desativado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="c0c27-183">1,4 Xbox 360 controlador comum para \[ requisito condicional do Windows\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-184">Windows 7</span></span><br/> <span data-ttu-id="c0c27-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-185">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-187">Jogos que dão suporte a controladores de gamepad devem dar suporte ao controlador Xbox 360 para Windows usando a API XInput.</span><span class="sxs-lookup"><span data-stu-id="c0c27-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="c0c27-188">Todas as referências a gatilhos e botões comuns do controlador devem usar os nomes do Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="c0c27-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-189">Inicie o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-189">Launch the game.</span></span></li>
<li><span data-ttu-id="c0c27-190">Vá para as opções do controlador.</span><span class="sxs-lookup"><span data-stu-id="c0c27-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="c0c27-191">Verifique se o jogo reconhece o controlador Xbox 360 para Windows como um dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0c27-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="c0c27-192">Jogue e verifique se o jogo e o sistema de menus são controláveis com o controlador Xbox 360 para Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="c0c27-193">Verifique se o controlador Xbox 360 para Windows se comporta de acordo com os padrões aceitos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="c0c27-194">(B para voltar, A para aceitar, inicie o no menu do jogo/Pause ou aceite, etc.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="c0c27-195">Verifique se o jogo refere-se aos botões do controlador e aos gatilhos usando os nomes do Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="c0c27-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-196">Se o jogo não dá suporte a um controlador de jogo e/ou só dá suporte ao teclado/mouse, ignore este caso de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="c0c27-197">\* \* As configurações do controlador podem estar localizadas fora do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="c0c27-198">1,5 várias taxas de proporção e resoluções</span><span class="sxs-lookup"><span data-stu-id="c0c27-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-199">Windows 7</span></span><br/> <span data-ttu-id="c0c27-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-200">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-202">O jogo deve dar suporte a pelo menos as seguintes taxas de proporção e resoluções de tela associadas:</span><span class="sxs-lookup"><span data-stu-id="c0c27-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="c0c27-203">4:3 &quot; normal &quot; (800 600 ou 1024 768)</span><span class="sxs-lookup"><span data-stu-id="c0c27-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="c0c27-204">16:9 &quot; widescreen &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="c0c27-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="c0c27-205">16:10 &quot; widescreen &quot; (1152 720, 1680 1050 ou 800 480)</span><span class="sxs-lookup"><span data-stu-id="c0c27-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-206">Localize as opções de vídeo para o jogo (isso pode estar em nosso jogo).</span><span class="sxs-lookup"><span data-stu-id="c0c27-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-207">Os testes a seguir devem ser feitos em um monitor widescreen.</span><span class="sxs-lookup"><span data-stu-id="c0c27-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="c0c27-208">Na seção resolução de vídeo, selecione 800 600 ou 1024 768.</span><span class="sxs-lookup"><span data-stu-id="c0c27-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="c0c27-209">Verifique se o jogo é executado a uma resolução de proporção de 4:3.</span><span class="sxs-lookup"><span data-stu-id="c0c27-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="c0c27-210">Na seção resolução de vídeo, selecione 1280 720.</span><span class="sxs-lookup"><span data-stu-id="c0c27-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="c0c27-211">Verifique se o jogo é executado a uma resolução de proporção de 16:9.</span><span class="sxs-lookup"><span data-stu-id="c0c27-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="c0c27-212">Na seção resolução de vídeo, selecione 1680 1050, 800 480 ou 1152 720.</span><span class="sxs-lookup"><span data-stu-id="c0c27-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="c0c27-213">Verifique se o jogo é executado a uma resolução de proporção de 16:10.</span><span class="sxs-lookup"><span data-stu-id="c0c27-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="c0c27-214">Verifique se o jogo não amplia a imagem e, por sua vez, apresenta uma área mais ampla de exibição.</span><span class="sxs-lookup"><span data-stu-id="c0c27-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="c0c27-215">Verifique se o jogo solicita o usuário quando uma alteração é feita na resolução.</span><span class="sxs-lookup"><span data-stu-id="c0c27-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="c0c27-216">Se o usuário não aceitar dentro de 15 segundos, verifique se a exibição é revertida para a configuração anterior.</span><span class="sxs-lookup"><span data-stu-id="c0c27-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="c0c27-217">Verifique se o jogo não adiciona barras pretas à esquerda e à direita da área de jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="c0c27-218">(Nesse caso, você verá a área do jogo ainda em uma proporção de 4:3 no meio da tela.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="c0c27-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="c0c27-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="c0c27-220">Esse requisito foi desativado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="c0c27-221">Requisito condicional de 1,7 Direct3D \[\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="c0c27-222">SO</span><span class="sxs-lookup"><span data-stu-id="c0c27-222">OS</span></span>                                                                    | <span data-ttu-id="c0c27-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c27-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c27-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-224">Windows 7</span></span><br/> <span data-ttu-id="c0c27-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-225">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-226">Windows XP</span></span><br/> | <span data-ttu-id="c0c27-227">Se o jogo usar o Direct3D, a versão mínima com suporte deverá ser o Direct3D 9 e o Direct3D deverá ser o padrão para qualquer opção de configuração de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="c0c27-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span><span class="sxs-lookup"><span data-stu-id="c0c27-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="c0c27-229">Inicie o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-229">Launch the game.</span></span> <span data-ttu-id="c0c27-230">Nas opções de vídeo, verifique se há opções de processamento, D3D e/ou OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c0c27-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="c0c27-231">Se houver, verifique se as opções de processamento do jogo são padrão para Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c0c27-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="c0c27-232">Se não for possível verificar se D3D9 é a versão do DirectX que está sendo usada, prossiga para o teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="c0c27-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt></span><span class="sxs-lookup"><span data-stu-id="c0c27-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="c0c27-234">Usar ferramenta: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="c0c27-235">1,8 habilitar reconhecimento de DPI alta</span><span class="sxs-lookup"><span data-stu-id="c0c27-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-236">Windows 7</span></span><br/> <span data-ttu-id="c0c27-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-238">Jogos e seus instaladores devem ser executados corretamente sem problemas visuais quando o dimensionamento de DPI estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="c0c27-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="c0c27-240">Defina o sistema como DPI 150%:</span><span class="sxs-lookup"><span data-stu-id="c0c27-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="c0c27-241">Windows Vista: painel de controle: personalização, ajustar tamanho da fonte (DPI), DPI personalizado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="c0c27-242">Defina como 150%.</span><span class="sxs-lookup"><span data-stu-id="c0c27-242">Set to 150%.</span></span><br/> <span data-ttu-id="c0c27-243">Windows 7: painel de controle: Exibir, definido como maior – 150%.</span><span class="sxs-lookup"><span data-stu-id="c0c27-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="c0c27-244">Execute o processo de instalação e o jogo para verificar se não há problemas com telas recortadas ou caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="c0c27-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="c0c27-246">Verifique se o elemento <dpiAware>true</dpiAware> está contido no manifesto inserido.</span><span class="sxs-lookup"><span data-stu-id="c0c27-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="c0c27-247">Usar ferramenta: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="c0c27-248">2. segurança e compatibilidade</span><span class="sxs-lookup"><span data-stu-id="c0c27-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="c0c27-249">2,1 seguir as diretrizes de controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c0c27-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-250">Windows 7</span></span><br/> <span data-ttu-id="c0c27-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-252">Cada arquivo executável (extensão .EXE) incluído com um aplicativo deve ter um manifesto inserido que define seu nível de execução:</span><span class="sxs-lookup"><span data-stu-id="c0c27-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-253">Para instaladores de jogos e jogos, o uiAccess sempre deve ser definido como &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="c0c27-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-254">Verifique se os arquivos executáveis do jogo contêm manifestos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="c0c27-255">Verifique se o manifesto do arquivo executável do jogo requestedExecutionLevel é &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="c0c27-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="c0c27-256">Usar ferramenta: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="c0c27-257">2,2 suporte a versões x64 do Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-258">Windows 7</span></span><br/> <span data-ttu-id="c0c27-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-260">Para manter a compatibilidade com as versões x64 do Windows:</span><span class="sxs-lookup"><span data-stu-id="c0c27-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="c0c27-261">Os títulos e os instaladores de título não devem conter nenhum código de 16 bits nem contar com nenhum componente de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c0c27-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="c0c27-262">Se o jogo for dependente dos drivers do modo kernel para a operação, as versões x64 desses drivers deverão estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c0c27-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="c0c27-263">A instalação do jogo deve detectar e instalar os drivers e componentes adequados para as edições de 64 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-264">O suporte para a edição de 64 bits do Windows XP Professional é opcional.</span><span class="sxs-lookup"><span data-stu-id="c0c27-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-265">Teste manual</span><span class="sxs-lookup"><span data-stu-id="c0c27-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-266">Execute o jogo em edições de 64 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="c0c27-267">Verifique se o processo de instalação do jogo é executado normalmente em edições de 64 bits do Windows Vista ou do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0c27-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="c0c27-268">Verifique se o jogo não encontrou um erro como resultado de executáveis de 16 bits em edições de 64 bits do Windows Vista ou do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0c27-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="c0c27-269">O erro irá mencionar o aplicativo de 16 bits na janela de erro.</span><span class="sxs-lookup"><span data-stu-id="c0c27-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="c0c27-270">Se o jogo tiver um executável de 64 bits nativo, use-o também.</span><span class="sxs-lookup"><span data-stu-id="c0c27-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="c0c27-271">2,3 assinar arquivos</span><span class="sxs-lookup"><span data-stu-id="c0c27-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-272">Windows 7</span></span><br/> <span data-ttu-id="c0c27-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-273">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-275">Todos os arquivos de código executáveis (por exemplo, .exe e extensões de .dll) devem ser assinados com um certificado Authenticode.</span><span class="sxs-lookup"><span data-stu-id="c0c27-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="c0c27-276">Se você estiver usando Windows Installer, os arquivos de pacote do instalador (arquivos de .msi) deverão ser assinados.</span><span class="sxs-lookup"><span data-stu-id="c0c27-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-277">Teste manual</span><span class="sxs-lookup"><span data-stu-id="c0c27-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-278">Navegue até o diretório do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="c0c27-279">Localize todos os arquivos de .exe e .dll.</span><span class="sxs-lookup"><span data-stu-id="c0c27-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="c0c27-280">Clique com o botão direito do mouse em Propriedades em cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="c0c27-281">Verifique se os arquivos executáveis do jogo contêm uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="c0c27-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="c0c27-282">Drivers de assinatura 2,4</span><span class="sxs-lookup"><span data-stu-id="c0c27-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-283">Windows 7</span></span><br/> <span data-ttu-id="c0c27-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-284">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-286">Qualquer driver de modo kernel instalado pelo jogo deve ser assinado com um certificado de Authenticode válido publicamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="c0c27-287">Qualquer driver de dispositivo de hardware em modo kernel instalado pelo jogo deve ter uma assinatura da Microsoft obtida por meio do programa Windows Hardware Quality Labs (WHQL) ou Signature (assinatura de confiabilidade de driver).</span><span class="sxs-lookup"><span data-stu-id="c0c27-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-288">Teste manual</span><span class="sxs-lookup"><span data-stu-id="c0c27-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-289">Instale o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-289">Install the game.</span></span></li>
<li><span data-ttu-id="c0c27-290">Verifique se o processo de instalação do jogo não exibe caixas de diálogo de driver não assinados.</span><span class="sxs-lookup"><span data-stu-id="c0c27-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="c0c27-291">2,5 executar verificação de versão corretamente</span><span class="sxs-lookup"><span data-stu-id="c0c27-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-292">Windows 7</span></span><br/> <span data-ttu-id="c0c27-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-293">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-295">Os jogos não devem falhar na execução em sistemas operacionais futuros, conforme indicado pelas alterações no número de versão do Windows, a menos que o contrato de licença de usuário final proíba o uso em sistemas operacionais futuros.</span><span class="sxs-lookup"><span data-stu-id="c0c27-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="c0c27-296">Se o jogo for supostamente reprovado, ele deverá fazer isso normalmente exibindo uma mensagem ao usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="c0c27-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="c0c27-298">Instale o jogo no Windows XP, nas edições de 32 bits do Windows Vista e do Windows 7, e nas edições de 64 bits do Windows Vista e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0c27-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="c0c27-299">Verifique se o processo de instalação do jogo não encontrou um erro relacionado à versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c0c27-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="c0c27-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="c0c27-301">Usar ferramenta: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="c0c27-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-302">Iniciar Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="c0c27-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="c0c27-303">Habilita o teste Compatibility:HighVersionLie depois de selecionar o INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="c0c27-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="c0c27-304">Instale o jogo e verifique se ele não bloqueia a instalação com base na versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c0c27-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="c0c27-305">Habilita o teste Compatibility:HighVersionLie depois de selecionar o GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="c0c27-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="c0c27-306">Execute o jogo e verifique se ele não bloqueia a execução com base na versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c0c27-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="c0c27-307">2.6 Suporte a sessões de usuário simultâneas</span><span class="sxs-lookup"><span data-stu-id="c0c27-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-308">Windows 7</span></span><br/> <span data-ttu-id="c0c27-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-309">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-311">Os jogos devem dar suporte a cenários padrão de multitarefa do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-312">Crie uma conta de usuário padrão no Windows Vista ou no Windows 7 chamada Mail.</span><span class="sxs-lookup"><span data-stu-id="c0c27-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="c0c27-313">Iniciar -> Painel de Controle -> adicionar ou remover contas de usuário -> criar nova conta</span><span class="sxs-lookup"><span data-stu-id="c0c27-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="c0c27-314">Iniciar o jogo como User Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="c0c27-315">ALT+TAB de volta para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0c27-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="c0c27-316">Verifique se o jogo corretamente ALT+TABs para a área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="c0c27-317">Clique em Iniciar -> [seta à direita de Bloqueio] -> Alternar Usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="c0c27-318">Faça logoff como User Ltda.</span><span class="sxs-lookup"><span data-stu-id="c0c27-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="c0c27-319">Verifique se o jogo é lançado como User Jane enquanto ainda está em execução como User Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="c0c27-320">Verifique se o jogo não encontra erros para User Jane ou User Jane durante o processo de troca de usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="c0c27-321">Se você puder iniciar outra sessão de jogo, verifique se não consegue ouvir áudio da sessão original do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="c0c27-322">Feche o jogo e volte para o usuário e o jogo originais.</span><span class="sxs-lookup"><span data-stu-id="c0c27-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="c0c27-323">2.7 Suporte a nomes longos</span><span class="sxs-lookup"><span data-stu-id="c0c27-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-324">Windows 7</span></span><br/> <span data-ttu-id="c0c27-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-325">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-327">Se um jogo dá suporte à salvação de arquivos, ele deve ser capaz de salvar arquivos que têm nomes e caminhos longos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="c0c27-328">O jogo deve lidar corretamente com caracteres especiais do sistema de arquivos, como \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="c0c27-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="c0c27-329">&quot; < ou > campos de entrada do usuário usados para criar nomes de arquivo ou caminhos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-330">Iniciar o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-330">Launch the game.</span></span></li>
<li><span data-ttu-id="c0c27-331">Inicie um novo jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-331">Start a new game.</span></span></li>
<li><span data-ttu-id="c0c27-332">Salve o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-332">Save the game.</span></span> <span data-ttu-id="c0c27-333">Durante o processo de salvar, verifique se o jogo salva usando o nome de salvar: Meu Primeiro Jogo de Salvar.</span><span class="sxs-lookup"><span data-stu-id="c0c27-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="c0c27-334">Saia de volta para o menu principal.</span><span class="sxs-lookup"><span data-stu-id="c0c27-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="c0c27-335">Tente carregar o jogo salvo recentemente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="c0c27-336">Verifique se o jogo não encontra erros ao manipular caracteres do sistema de arquivos sem suporte, como \ /: \* ?</span><span class="sxs-lookup"><span data-stu-id="c0c27-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="c0c27-337">&quot; < ou > se o jogo permitir, nomeia o jogo salvo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="c0c27-338">Se o usuário tiver permissão para nomear seu perfil e/ou caractere ou salvar jogos, verifique se o jogo não encontra erros ao usar nomes de arquivo longos aqui também.</span><span class="sxs-lookup"><span data-stu-id="c0c27-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="c0c27-339">3. Instalação</span><span class="sxs-lookup"><span data-stu-id="c0c27-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="c0c27-340">3.1 Instalação fácil</span><span class="sxs-lookup"><span data-stu-id="c0c27-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-341">Windows 7</span></span><br/> <span data-ttu-id="c0c27-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-342">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-344">Jogos com uma instalação tradicional devem fornecer um caminho simplificado em sua interface do usuário de instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-345">Insira o disco do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="c0c27-346">Verifique se o jogo não exibe mais de um contrato End-User licença (EULA).</span><span class="sxs-lookup"><span data-stu-id="c0c27-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="c0c27-347">Se o jogo dá suporte a uma opção de instalação personalizada ou avançada, verifique se essa opção está acessível durante o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="c0c27-348">Verifique se a opção Instalação padrão ignora todas as seleções de entrada do usuário para o processo de instalação (seleção de pasta de instalação, seleção de componentes e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c0c27-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="c0c27-349">Verifique se o processo de instalação do jogo não solicita a instalação do componente do sistema operacional (instalação do DirectX, Runtimes do Visual C e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c0c27-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="c0c27-350">Verifique se o processo de instalação do jogo não solicita a interação do firewall.</span><span class="sxs-lookup"><span data-stu-id="c0c27-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="c0c27-351">Verifique se o jogo é executado automaticamente ou se um menu do launcher está presente no final do processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="c0c27-352">Verifique se o processo de desinstalação do jogo remove todos os arquivos de componente do sistema operacional instalados e não redistribuídos e limpa todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="c0c27-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="c0c27-353">Limpar todas as configurações e dados por usuário (como jogos salvos) não é necessário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="c0c27-354">3.2 Dar suporte ao controle de conta de usuário para instalação</span><span class="sxs-lookup"><span data-stu-id="c0c27-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-355">Windows 7</span></span><br/> <span data-ttu-id="c0c27-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="c0c27-357">O instalador do jogo não deve supor que ele está em execução no mesmo contexto que o usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="c0c27-358">Portanto, os jogos devem executar tarefas por usuário na primeira execução separadamente da instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-359">Verifique se você pode instalar o jogo como User Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="c0c27-360">(Isso exigirá direitos elevados durante o processo de instalação/instalação.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="c0c27-361">Verifique se o processo de instalação do jogo solicita que a Usuária Jane eleve por meio de Credenciais de Administrador.</span><span class="sxs-lookup"><span data-stu-id="c0c27-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="c0c27-362">(O prompt a ser elevado será a seguir quando o usuário tentar instalar.)</span><span class="sxs-lookup"><span data-stu-id="c0c27-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="c0c27-363">Opte por Autorun do jogo no final da instalação, se ele ainda não fizer isso, ou inspecioná-lo no menu exibido.</span><span class="sxs-lookup"><span data-stu-id="c0c27-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="c0c27-364">Uma vez no jogo, crie um novo perfil, reproduza e salve um jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="c0c27-365">Saia do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-365">Exit the game.</span></span></li>
<li><span data-ttu-id="c0c27-366">Reinicie o jogo e verifique se os Perfis de Usuário e Os Jogos Salvos podem ser acessados pela conta do Usuário Jane.</span><span class="sxs-lookup"><span data-stu-id="c0c27-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="c0c27-367">3.3 Instalar para corrigir pastas</span><span class="sxs-lookup"><span data-stu-id="c0c27-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-368">Windows 7</span></span><br/> <span data-ttu-id="c0c27-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-369">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-371">Os jogos devem ser instalados na pasta Arquivos de Programas por padrão.</span><span class="sxs-lookup"><span data-stu-id="c0c27-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="c0c27-372">Os dados do usuário devem ser gravados na primeira operação e não durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-373">Instale o jogo usando o tipo de instalação Padrão.</span><span class="sxs-lookup"><span data-stu-id="c0c27-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="c0c27-374">Verifique se o jogo foi instalado nos Arquivos de Programas.</span><span class="sxs-lookup"><span data-stu-id="c0c27-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-375">Se esse teste falhar, verifique se o jogo se destina à instalação para Todos os Usuários.</span><span class="sxs-lookup"><span data-stu-id="c0c27-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="c0c27-376">Nesse caso, isso é uma falha.</span><span class="sxs-lookup"><span data-stu-id="c0c27-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="c0c27-377">3.4 Instalar corretamente os recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-378">Windows 7</span></span><br/> <span data-ttu-id="c0c27-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-379">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-381">Os aplicativos não devem tentar instalar arquivos ou chaves do Registro protegidos pelo PROTEÇÃO DE RECURSOS DO WINDOWS (WRP).</span><span class="sxs-lookup"><span data-stu-id="c0c27-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="c0c27-382">Verifique se nenhuma Proteção de Recursos do Windows caixa de diálogo WRP aparecem durante o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="c0c27-383">3.5 Evitar reinicializações durante a instalação</span><span class="sxs-lookup"><span data-stu-id="c0c27-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-384">Windows 7</span></span><br/> <span data-ttu-id="c0c27-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-385">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-387">O instalador do jogo não deve supor que a instalação de componentes do Windows de pacotes de redistribuição exija uma reinicialização, a menos que a reinicialização seja indicada por um resultado de retorno ou pela documentação da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c0c27-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-388">Instale o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-388">Install the game.</span></span></li>
<li><span data-ttu-id="c0c27-389">Verifique se o jogo não exige que o sistema seja reinicializado após a instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-390">Se um REDIST de atualização do sistema da Microsoft exigir uma reinicialização, faça o seguinte: Concluir a instalação do jogo, desinstalar o jogo e reinstalar o jogo uma segunda vez.</span><span class="sxs-lookup"><span data-stu-id="c0c27-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="c0c27-391">O processo de instalação do jogo não deve exigir uma reinicialização nesta segunda instalação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="c0c27-392">3.6 Usar o versionamento de arquivo corretamente</span><span class="sxs-lookup"><span data-stu-id="c0c27-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-393">Windows 7</span></span><br/> <span data-ttu-id="c0c27-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-394">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-396">O programa de instalação do jogo deve verificar corretamente para garantir que as versões mais recentes do arquivo sejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="c0c27-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="c0c27-397">A instalação de um jogo nunca deve regredir os arquivos que você não produz ou que são compartilhados por aplicativos que você não produz.</span><span class="sxs-lookup"><span data-stu-id="c0c27-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-398">Antes de instalar o jogo, crie um instantâneo de pré-instalação do System32.</span><span class="sxs-lookup"><span data-stu-id="c0c27-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-399">Faça um diretório chamado G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="c0c27-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="c0c27-400">Abrir uma janela de comando (Iniciar -> Executar -> cmd).</span><span class="sxs-lookup"><span data-stu-id="c0c27-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="c0c27-401">Navegue até c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="c0c27-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="c0c27-402">Digite dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="c0c27-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="c0c27-403">Crie um instantâneo pós-instalação do System32.</span><span class="sxs-lookup"><span data-stu-id="c0c27-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="c0c27-404">Abrir uma janela de comando (Iniciar -> Executar -> cmd).</span><span class="sxs-lookup"><span data-stu-id="c0c27-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="c0c27-405">Navegue até c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="c0c27-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="c0c27-406">Digite dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="c0c27-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="c0c27-407">Verifique se o jogo não regrediu nenhuma versão de arquivo de arquivos que o jogo não produziu (... dos arquivos listados nos dois documentos comparando pregame.txt com postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="c0c27-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="c0c27-408">3.7 Dar suporte ao requisito condicional de autorun \[\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-409">Windows 7</span></span><br/> <span data-ttu-id="c0c27-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-410">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-412">Para jogos distribuídos em CD, DVD ou outra mídia removível que suportam a Autorun, quando o disco é inserido pela primeira vez, o aplicativo deve ser executado automaticamente ou solicitar que o usuário instale o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-413">Programas de execução automática que foram escritos para uso em versões do Windows anteriores ao Windows Vista não devem usar o runtime do .NET, pois essa tecnologia não está incluída no Windows XP ou em versões mais antigas do Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="c0c27-414">Para obter mais diretrizes, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Jogos para Requisitos Técnicos</a> do Windows 3.7, Suporte a Autorun.</span><span class="sxs-lookup"><span data-stu-id="c0c27-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="c0c27-415">Insira o disco ou a mídia do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="c0c27-416">Verifique se a caixa de diálogo instalar/executar é exibida automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="c0c27-417">Windows Vista ou Windows 7: verifique se o próprio programa de autorun do jogo não solicita que a Usuária Jane eleve por meio de Credenciais de Administrador.</span><span class="sxs-lookup"><span data-stu-id="c0c27-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="c0c27-418">Verifique se o executável De execução automática não precisa de componentes REDIST in-box, como bibliotecas .NET 3.5, C Run-Time e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c0c27-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="c0c27-419">Verifique se a inserção do disco novamente na unidade após a instalação não faz com que a instalação seja iniciada automaticamente novamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="c0c27-420">4. Confiabilidade</span><span class="sxs-lookup"><span data-stu-id="c0c27-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="c0c27-421">4.1 Eliminar reinicializações desnecessárias</span><span class="sxs-lookup"><span data-stu-id="c0c27-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="c0c27-422">SO</span><span class="sxs-lookup"><span data-stu-id="c0c27-422">OS</span></span>                                              | <span data-ttu-id="c0c27-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c27-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c27-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-424">Windows 7</span></span><br/> <span data-ttu-id="c0c27-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-425">Windows Vista</span></span><br/> | <span data-ttu-id="c0c27-426">Todos os instaladores de aplicativos devem aproveitar as APIs do Gerenciador de Reinicialização para evitar reinicializações do sistema (consulte [o requisito 3.5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="c0c27-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="c0c27-427">4.2 Eliminar Application Verifier falhas</span><span class="sxs-lookup"><span data-stu-id="c0c27-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-428">Windows 7</span></span><br/> <span data-ttu-id="c0c27-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-429">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-431">O jogo não deve gerar falhas em execução no Microsoft Application Verifier (AppVerifier), versão 4.0 ou posterior, nos seguintes testes:</span><span class="sxs-lookup"><span data-stu-id="c0c27-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="c0c27-432">Noções básicas: Handles, Heaps, Locks, Memory, TLS</span><span class="sxs-lookup"><span data-stu-id="c0c27-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="c0c27-433">Diversos: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="c0c27-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-434">Ferramenta de Uso: AppVerifier 4.0 (ou posterior)</span><span class="sxs-lookup"><span data-stu-id="c0c27-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="c0c27-435">Instale AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="c0c27-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="c0c27-436">Iniciar AppVerifier e selecionar Arquivo -> Adicionar Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="c0c27-437">Localize o executável do jogo, selecione-o e clique no &quot; botão &quot; Abrir.</span><span class="sxs-lookup"><span data-stu-id="c0c27-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="c0c27-438">Na seção &quot; &quot; Aplicativos, selecione o executável do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="c0c27-439">Na seção Testes, selecione os testes listados acima nas categorias Básico e &quot; &quot; &quot; &quot; &quot; Diversos (desmarque ThreadPool e TimeRollOver) e verifique se todos os outros testes não &quot; estão selecionados.</span><span class="sxs-lookup"><span data-stu-id="c0c27-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="c0c27-440">Iniciar o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-440">Launch the game.</span></span></li>
<li><span data-ttu-id="c0c27-441">Verifique se o jogo não gera falhas quando executado em Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="c0c27-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0c27-442">Alguns testes exigem que um depurador seja totalmente executado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="c0c27-443">Isso pode exigir uma versão de lançamento desprotegida do executável do jogo, já que a tecnologia anti-fraude/antileitura pode interferir no AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="c0c27-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="c0c27-444">4.3 Suporte a Relatório de Erros do Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-445">Windows 7</span></span><br/> <span data-ttu-id="c0c27-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-446">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-448">Os jogos devem lidar apenas com exceções conhecidas e esperadas e Relatório de Erros do Windows não devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="c0c27-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="c0c27-449">Se uma falha (como uma violação de acesso) for injetada em um jogo, ela deverá permitir Relatório de Erros do Windows relatar a falha.</span><span class="sxs-lookup"><span data-stu-id="c0c27-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="c0c27-450">Ferramenta use: seqüestrador de threads</span><span class="sxs-lookup"><span data-stu-id="c0c27-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="c0c27-451">Se o aplicativo falhar durante o teste, verifique se o jogo exibe Relatório de Erros do Windows corretamente e coleta dados de falha.</span><span class="sxs-lookup"><span data-stu-id="c0c27-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-452">Windows 7</span></span><br/> <span data-ttu-id="c0c27-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-453">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-455">Todos os arquivos executáveis (por exemplo, arquivos .exe ou .dll) devem conter um Nome do Produto, Nome da Empresa e Versão do Arquivo precisos.</span><span class="sxs-lookup"><span data-stu-id="c0c27-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="c0c27-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Teste manual:</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="c0c27-457">Clique com o botão direito do mouse nos arquivos executáveis do jogo na mídia de instalação e nos instalados no disco rígido do computador.</span><span class="sxs-lookup"><span data-stu-id="c0c27-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="c0c27-458">Selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0c27-458">Select Properties.</span></span></li>
<li><span data-ttu-id="c0c27-459">Windows XP: clique na <strong>guia</strong> Versão. Verifique se os campos Nome do Produto, Nome da Empresa e Versão do Arquivo estão preenchidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="c0c27-460">Windows Vista ou Windows 7: clique na <strong>guia</strong> Detalhes. Verifique se os campos Nome do produto e Versão do Arquivo estão preenchidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="c0c27-461">O Nome da Empresa não está visível na página de propriedades do Windows Vista ou do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0c27-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="c0c27-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Teste automatizado:</dt> </span><span class="sxs-lookup"><span data-stu-id="c0c27-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="c0c27-463">Use a Ferramenta de Teste do Microsoft Games for Windows; consulte <a href="#64-microsoft-games-for-windows-test-tool">a seção 6.4</a>.</span><span class="sxs-lookup"><span data-stu-id="c0c27-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c27-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-464">Windows 7</span></span><br/> <span data-ttu-id="c0c27-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c27-465">Windows Vista</span></span><br/> <span data-ttu-id="c0c27-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="c0c27-467">A saída normal do jogo não deve resultar em uma falha de exceção desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c0c27-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="c0c27-468">Depois de jogar o jogo para uma sessão de jogos normal, verifique se o jogo não gera erros na saída.</span><span class="sxs-lookup"><span data-stu-id="c0c27-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="c0c27-469">5. Script de teste de exemplo</span><span class="sxs-lookup"><span data-stu-id="c0c27-469">5. Sample Test Script</span></span>

<span data-ttu-id="c0c27-470">Este é um exemplo de uma passagem de teste típica usando os requisitos de teste anteriores como um guia.</span><span class="sxs-lookup"><span data-stu-id="c0c27-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="c0c27-471">5.1 Ferramentas</span><span class="sxs-lookup"><span data-stu-id="c0c27-471">5.1 Tools</span></span>

-   <span data-ttu-id="c0c27-472">Edição de 32 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU AMD</span><span class="sxs-lookup"><span data-stu-id="c0c27-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="c0c27-473">Edição de 32 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU Intel</span><span class="sxs-lookup"><span data-stu-id="c0c27-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="c0c27-474">Edição de 64 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU AMD</span><span class="sxs-lookup"><span data-stu-id="c0c27-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="c0c27-475">Edição de 64 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU Intel</span><span class="sxs-lookup"><span data-stu-id="c0c27-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="c0c27-476">Edição de 32 bits Windows XP SP2 em uma CPU AMD</span><span class="sxs-lookup"><span data-stu-id="c0c27-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="c0c27-477">Edição de 32 bits Windows XP SP2 em uma CPU Intel</span><span class="sxs-lookup"><span data-stu-id="c0c27-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="c0c27-478">Monitor de Tela Larga que dá suporte a 1680 1050</span><span class="sxs-lookup"><span data-stu-id="c0c27-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="c0c27-479">Xbox 360 controlador para Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="c0c27-480">5.2 Pré-instalação</span><span class="sxs-lookup"><span data-stu-id="c0c27-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="c0c27-481">Windows Vista e Windows 7: criar dois usuários padrão: Jane e Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="c0c27-482">Windows Vista e Windows 7: verifique se o Controle de Conta de Usuário está habilitado</span><span class="sxs-lookup"><span data-stu-id="c0c27-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="c0c27-483">Criar um instantâneo de pré-instalação do System32</span><span class="sxs-lookup"><span data-stu-id="c0c27-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="c0c27-484">Fazer um diretório chamado G4Wtest</span><span class="sxs-lookup"><span data-stu-id="c0c27-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="c0c27-485">Abrir uma janela de comando (Iniciar -> Executar -> cmd)</span><span class="sxs-lookup"><span data-stu-id="c0c27-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="c0c27-486">Navegue até c: \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="c0c27-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="c0c27-487">Digite dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="c0c27-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="c0c27-488">Windows Vista e Windows 7: definido como 150% DPI \[ 1.8\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="c0c27-489">Vá para [Instalar](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="c0c27-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="c0c27-490">5.3 Instalar</span><span class="sxs-lookup"><span data-stu-id="c0c27-490">5.3 Install</span></span>

1.  <span data-ttu-id="c0c27-491">Fazer logoff como User Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="c0c27-492">Insira o disco do jogo na unidade de CD/DVD, verifique se a caixa de diálogo instalar/executar é exibida automaticamente \[ 3.7\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="c0c27-493">Verifique se o processo de instalação do jogo solicita que a Usuária Jane eleve as Credenciais \[ de Administrador 3.2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="c0c27-494">Verifique se o próprio programa de autorun do jogo não solicita que a Usuária Jane eleve por meio de Credenciais de Administrador \[ 3.7\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="c0c27-495">Verifique se o jogo não exibe mais de um End-User EULA (Contrato de Licença) \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="c0c27-496">Verifique se o jogo exibe as opções de instalação Padrão/Fácil e Personalizada/Avançada \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="c0c27-497">Verifique se a opção instalação Padrão/Fácil ignora todas as seleções de entrada do usuário para o processo de instalação (seleção de pasta de instalação, seleção de componentes e assim por diante).) \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="c0c27-498">Verifique se o processo de instalação do jogo não solicita a instalação do componente do sistema operacional (instalação do DirectX, bibliotecas de Run-Time C e assim por diante).) \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="c0c27-499">Verifique se o processo de instalação do jogo não solicita a interação do firewall \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="c0c27-500">Verifique se o processo de instalação do jogo não encontra um erro em relação à \[ versão 2.5 \] \[ 4.2 do sistema operacional\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="c0c27-501">Verifique se o processo de instalação do jogo não exibe caixas de diálogo (s) de driver não assinado \[ 2,4\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="c0c27-502">Verifique se nenhuma caixa de diálogo Proteção de Recursos do Windows (WRP) aparece durante o processo de instalação \[ 3,4\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="c0c27-503">Verifique se inserindo novamente o disco na unidade após a instalação não faz com que a instalação seja iniciada automaticamente</span><span class="sxs-lookup"><span data-stu-id="c0c27-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="c0c27-504">Verifique se o jogo não exige que o sistema seja reinicializado após a instalação \[ 3,5\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="c0c27-505">Verifique se você pode instalar o jogo como o usuário Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="c0c27-506">Verifique se o jogo é executado automaticamente ou se um menu do inicializador está presente no final do processo de instalação \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="c0c27-507">Se o jogo executar automaticamente após a instalação, pule para [tempo de execução](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="c0c27-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="c0c27-508">Se o jogo deixasse um menu de inicialização para cima ou falhou ao desinstalar, consulte [a seção pós-instalação](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="c0c27-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="c0c27-509">5,4 pós-instalação</span><span class="sxs-lookup"><span data-stu-id="c0c27-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="c0c27-510">Verifique se o jogo não coloca os atalhos de inicialização no usuário área de trabalho \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="c0c27-511">Verifique se o jogo não coloca os atalhos de inicialização no menu iniciar \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="c0c27-512">Verifique se o ícone de jogo é exibido no explorador de jogos do Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="c0c27-513">Verifique se os metadados (Publicador, desenvolvedor, gênero, data de lançamento, versão) na parte inferior são exibidos e estão corretos \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="c0c27-514">Verifique se o ícone de jogo exibe informações do WEI (índice de experiência do Windows) no explorador de jogos do Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="c0c27-515">Verifique se os hiperlinks de jogos para os metadados funcionam corretamente no explorador de jogos do Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="c0c27-516">Verifique se o jogo exibe a classificação de controle dos pais preciso no explorador de jogos do Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="c0c27-517">Criar um instantâneo pós-instalação de system32</span><span class="sxs-lookup"><span data-stu-id="c0c27-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="c0c27-518">Exibir uma janela de comando (Start-> execute-> cmd)</span><span class="sxs-lookup"><span data-stu-id="c0c27-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="c0c27-519">Navegue até c: \\ Windows \\ System32</span><span class="sxs-lookup"><span data-stu-id="c0c27-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="c0c27-520">Digite dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="c0c27-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="c0c27-521">Verifique se o jogo não retorna nenhuma versão de arquivo dos arquivos listados nos dois documentos, comparando pregame.txt a postgame.txt \[ 3,6\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="c0c27-522">Continuar em [tempo de execução](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="c0c27-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="c0c27-523">5,5 tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c0c27-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="c0c27-524">TEMPO de execução 1: se o menu iniciar estiver presente, inicie o jogo a partir daí.</span><span class="sxs-lookup"><span data-stu-id="c0c27-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="c0c27-525">Se o jogo for executado automaticamente ou tiver sido iniciado no menu do inicializador de jogos após a instalação, execute o seguinte: caso contrário, pule para o tempo de execução 2:</span><span class="sxs-lookup"><span data-stu-id="c0c27-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="c0c27-526">Criar um perfil (se o jogo permitir)</span><span class="sxs-lookup"><span data-stu-id="c0c27-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="c0c27-527">Iniciar um novo jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-527">Start a new game</span></span>
    3.  <span data-ttu-id="c0c27-528">Salvar o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-528">Save the game</span></span>
    4.  <span data-ttu-id="c0c27-529">Sair do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-529">Exit the game</span></span>
    5.  <span data-ttu-id="c0c27-530">Iniciar o jogo no explorador de jogos</span><span class="sxs-lookup"><span data-stu-id="c0c27-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="c0c27-531">Verifique se o jogo é iniciado no ícone do explorador de jogos \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="c0c27-532">Verifique se o jogo não solicita credenciais de administrador na inicialização \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="c0c27-533">Verifique se os perfis de usuário e os jogos salvos podem ser acessados pelo usuário Carina conta \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="c0c27-534">Prosseguir para o tempo de execução 3</span><span class="sxs-lookup"><span data-stu-id="c0c27-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="c0c27-535">TEMPO de execução 2: se o jogo não executar automaticamente ou exibir uma inicialização no menu do inicializador de jogos, isso é uma falha de \[ 3,1 \] ; no entanto, o teste pode continuar normalmente:</span><span class="sxs-lookup"><span data-stu-id="c0c27-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="c0c27-536">Iniciar o jogo no explorador de jogos</span><span class="sxs-lookup"><span data-stu-id="c0c27-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="c0c27-537">Verifique se o jogo é iniciado no ícone do explorador de jogos \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="c0c27-538">Verifique se o jogo não solicita credenciais de administrador na inicialização \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="c0c27-539">Prosseguir para o tempo de execução 3</span><span class="sxs-lookup"><span data-stu-id="c0c27-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="c0c27-540">TEMPO de execução 3: se o jogo der suporte a um game pad, verifique se o jogo reconhece o controlador Xbox 360 para Windows como um dispositivo de entrada \[ 1,4\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="c0c27-541">Se necessário, habilite o controlador por meio do menu de opções</span><span class="sxs-lookup"><span data-stu-id="c0c27-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="c0c27-542">Verifique se o jogo refere-se aos botões e gatilhos do controlador usando os nomes do Xbox 360</span><span class="sxs-lookup"><span data-stu-id="c0c27-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="c0c27-543">Verifique se o jogo e o sistema de menus são controláveis com o controlador Xbox 360 para Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="c0c27-544">Verifique se o controlador Xbox 360 para Windows se comporta de acordo com os padrões aceitos</span><span class="sxs-lookup"><span data-stu-id="c0c27-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="c0c27-545">Defina o vídeo como \[ 1,5 \] :</span><span class="sxs-lookup"><span data-stu-id="c0c27-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="c0c27-546">Verifique se o jogo é executado a uma resolução de proporção de 4:3 (800 600 ou 1024 768)</span><span class="sxs-lookup"><span data-stu-id="c0c27-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="c0c27-547">Verifique se o jogo é executado a uma resolução de proporção de 16:9 (1280 720)</span><span class="sxs-lookup"><span data-stu-id="c0c27-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="c0c27-548">Verifique se o jogo é executado a uma resolução de proporção de 16:10 (1680 1050, 800 480 ou 1152 720)</span><span class="sxs-lookup"><span data-stu-id="c0c27-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="c0c27-549">Verifique se o jogo solicita o usuário quando uma alteração é feita na resolução</span><span class="sxs-lookup"><span data-stu-id="c0c27-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="c0c27-550">Verifique se a exibição é revertida para a configuração anterior se você não aceitar dentro de 15 segundos</span><span class="sxs-lookup"><span data-stu-id="c0c27-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="c0c27-551">Verifique se o jogo não amplia a imagem e, por sua vez, apresenta uma área mais ampla de exibição</span><span class="sxs-lookup"><span data-stu-id="c0c27-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="c0c27-552">Verifique se o jogo não adiciona barras pretas à esquerda e à direita da área de jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="c0c27-553">Se estiver disponível nas configurações de vídeo, verifique se as opções de processamento do jogo são padrão para Direct3D \[ 1,7 \] ; caso contrário, prossiga para [testes automatizados](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="c0c27-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="c0c27-554">Se solicitado ou se a opção estiver disponível, crie um perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="c0c27-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="c0c27-555">Verifique se o jogo não encontrou erros ao usar nomes de arquivo longos \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="c0c27-556">Inicie um novo jogo, crie um jogo e verifique se o jogo não encontrou erros ao manipular os caracteres do sistema de arquivos sem suporte \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="c0c27-557">Verifique se o jogo ALT + TAB corretamente para a área de trabalho do Windows \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="c0c27-558">Alterne os usuários com o jogo em execução clicando em Iniciar-> Alternar usuário</span><span class="sxs-lookup"><span data-stu-id="c0c27-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="c0c27-559">Fazer logon como Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="c0c27-560">Verifique se o jogo é iniciado como usuário Toby enquanto ainda está em execução como usuário Jane \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="c0c27-561">Verifique se o jogo não encontra erros para o usuário Toby ou o usuário Jane durante o processo de mudança de usuário \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="c0c27-562">Verifique se você não consegue ouvir áudio da sessão de jogo original \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="c0c27-563">Sair do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-563">Exit the game</span></span>
    7.  <span data-ttu-id="c0c27-564">Fazer logoff de Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-564">Log off Toby</span></span>
    8.  <span data-ttu-id="c0c27-565">Voltar para o usuário original onde o jogo está em execução</span><span class="sxs-lookup"><span data-stu-id="c0c27-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="c0c27-566">ALT + TAB de volta ao jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="c0c27-567">Sair do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-567">Exit the game</span></span>
10. <span data-ttu-id="c0c27-568">Prosseguir para o [pós-tempo de execução](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="c0c27-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="c0c27-569">5,6 pós-tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c0c27-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="c0c27-570">Verifique se o jogo não gera erros na saída \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="c0c27-571">Verifique se o jogo instalado nos arquivos de programas \[ 3,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="c0c27-572">Ir para os [controles dos pais](/windows)</span><span class="sxs-lookup"><span data-stu-id="c0c27-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="c0c27-573">5,7 controles dos pais</span><span class="sxs-lookup"><span data-stu-id="c0c27-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="c0c27-574">Abrir controles dos pais no painel de controle</span><span class="sxs-lookup"><span data-stu-id="c0c27-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="c0c27-575">Verifique se o jogo exibe a classificação de controle dos pais preciso abaixo do título do jogo no painel de controle dos controles dos pais \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="c0c27-576">Consulte o caso de teste \[ 1,2 \] para os seguintes testes:</span><span class="sxs-lookup"><span data-stu-id="c0c27-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="c0c27-577">Depois de definir os controles dos pais como "on", verifique se o jogo é executado com essas configurações como o usuário Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="c0c27-578">Fazer logoff e logon como Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="c0c27-579">Verifique se o jogo é executado com essas configurações como usuário Toby \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="c0c27-580">Fazer logoff e logon como Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="c0c27-581">Na seção controle dos pais, bloqueie o usuário Toby de ver jogos um nível ESRB e superior do jogo que você acabou de instalar</span><span class="sxs-lookup"><span data-stu-id="c0c27-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="c0c27-582">Exemplo: se o jogo for classificado como E, defina-o para que Toby possa reproduzir jogos classificados como C</span><span class="sxs-lookup"><span data-stu-id="c0c27-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="c0c27-583">Verifique se o jogo é executado com essas configurações como o usuário Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="c0c27-584">Fazer logoff e logon como usuário Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="c0c27-585">Verifique se o jogo não é iniciado no usuário Toby quando ESRB está bloqueado pelo usuário Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="c0c27-586">Fazer logoff como usuário Toby e voltar como usuário Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="c0c27-587">Se alterado anteriormente, restaure as configurações de ESRB</span><span class="sxs-lookup"><span data-stu-id="c0c27-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="c0c27-588">Se não houver configurações de ESRB, selecione "bloquear ou permitir jogos específicos" e selecione o jogo por nome</span><span class="sxs-lookup"><span data-stu-id="c0c27-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="c0c27-589">Fazer logoff como Jane e on as Toby</span><span class="sxs-lookup"><span data-stu-id="c0c27-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="c0c27-590">Verifique se o jogo não é iniciado no usuário Toby quando o EXE/Name está bloqueado pelo usuário Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="c0c27-591">Fazer logoff como Toby e voltar como Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="c0c27-592">Como Jane, abra controles de usuário-> restrições de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0c27-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="c0c27-593">Clique em "Toby pode usar apenas os programas que eu permitir" e, em seguida, clique em OK (ou seja, não permitir nenhum EXEs)</span><span class="sxs-lookup"><span data-stu-id="c0c27-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="c0c27-594">Clique na caixa desmarcar tudo e, em seguida, clique em OK</span><span class="sxs-lookup"><span data-stu-id="c0c27-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="c0c27-595">Ir para controles de usuários controles de \| jogos e permitir o jogo específico usando a classificação ESRB</span><span class="sxs-lookup"><span data-stu-id="c0c27-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="c0c27-596">Faça logoff como Jane e faça logon como Toby e tente jogar o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="c0c27-597">Verifique se o jogo não está bloqueado e se o Toby pode reproduzi-lo quando "permitir nenhum EXEs" estiver definido \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="c0c27-598">Fazer logoff como usuário Toby e voltar como usuário Jane</span><span class="sxs-lookup"><span data-stu-id="c0c27-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="c0c27-599">Vá para controles dos pais no painel de controle e remova as restrições</span><span class="sxs-lookup"><span data-stu-id="c0c27-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="c0c27-600">Verifique se os dois usuários podem agora jogar o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="c0c27-601">Prosseguir para os [testes automatizados](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="c0c27-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="c0c27-602">5,8 testes automatizados</span><span class="sxs-lookup"><span data-stu-id="c0c27-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="c0c27-603">Verifique se o jogo não gera falhas quando executado em Application Verifier-consulte a documentação da ferramenta de teste de identidade visual \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="c0c27-604">Verifique se os arquivos executáveis do jogo contêm manifestos-consulte a documentação da ferramenta de teste de identidade visual \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="c0c27-605">Verifique se o manifesto do arquivo executável do jogo requestedExecutionLevel é "AsInvoker"-consulte a documentação da ferramenta de teste de identidade visual \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="c0c27-606">Prosseguir para [outros testes](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="c0c27-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="c0c27-607">5,9 outros testes</span><span class="sxs-lookup"><span data-stu-id="c0c27-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="c0c27-608">Verifique se os arquivos executáveis do jogo contêm uma assinatura digital \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="c0c27-609">Verifique se o processo de instalação do jogo é executado normalmente em edições de 64 bits do Windows Vista e/ou do Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="c0c27-610">Verifique se o jogo não encontrou um erro como resultado de executáveis de 16 bits em edições de 64 bits do Windows Vista e/ou do Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="c0c27-611">Forçar o aplicativo a falhar durante o teste e verificar se o jogo exibe Relatório de Erros do Windows corretamente e coleta os dados de falha \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="c0c27-612">Garantir resumos de arquivos apropriados \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="c0c27-613">Clique em Iniciar-> computador</span><span class="sxs-lookup"><span data-stu-id="c0c27-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="c0c27-614">Navegue até o diretório do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="c0c27-615">Na janela de pesquisa, digite \*.dll</span><span class="sxs-lookup"><span data-stu-id="c0c27-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="c0c27-616">Para cada arquivo: clique com o botão direito do mouse no arquivo e clique em Propriedades</span><span class="sxs-lookup"><span data-stu-id="c0c27-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="c0c27-617">No Windows XP: clique na guia versão. Verifique se os campos nome do produto, nome da empresa e versão do arquivo estão populados corretamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="c0c27-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-618">\[4.3\]</span></span>
        -   <span data-ttu-id="c0c27-619">No Windows Vista e no Windows 7: clique na guia detalhes. Verifique se os campos nome do produto e versão do arquivo estão populados corretamente.</span><span class="sxs-lookup"><span data-stu-id="c0c27-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="c0c27-620">O nome da empresa não está visível na página de propriedades do Windows Vista ou do Windows 7 \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="c0c27-621">Repita essa verificação para arquivos de .exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="c0c27-622">Inicie o jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-622">Launch the game.</span></span>

    1.  <span data-ttu-id="c0c27-623">Pressione CTRL + ALT + DEL</span><span class="sxs-lookup"><span data-stu-id="c0c27-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="c0c27-624">Clique na seta "opções de desligamento"</span><span class="sxs-lookup"><span data-stu-id="c0c27-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="c0c27-625">Clique em reiniciar</span><span class="sxs-lookup"><span data-stu-id="c0c27-625">Click Restart</span></span>
    4.  <span data-ttu-id="c0c27-626">Verificar se o jogo não bloqueia o desligamento \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="c0c27-627">Continuar a [desinstalação](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="c0c27-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="c0c27-628">5,10 desinstalar</span><span class="sxs-lookup"><span data-stu-id="c0c27-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="c0c27-629">Verifique se o processo de desinstalação do jogo remove todos os arquivos de componente do sistema operacional instalados e não redistribuídos e limpa todas as configurações \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="c0c27-630">Verifique no Windows Vista ou no Windows 7 se o painel de controle é a única maneira de remover o programa \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="c0c27-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="c0c27-631">Notas da ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="c0c27-631">Test Tool Notes</span></span>

<span data-ttu-id="c0c27-632">Estas são observações para cada uma das ferramentas de teste listadas nos requisitos de teste acima.</span><span class="sxs-lookup"><span data-stu-id="c0c27-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="c0c27-633">6,1 AppVerifier 4,0 (ou superior)</span><span class="sxs-lookup"><span data-stu-id="c0c27-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="c0c27-634">**Caso de teste: 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="c0c27-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="c0c27-635">Alguns aplicativos falham ao serem executados com o AppVerifier em execução, devido à proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="c0c27-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="c0c27-636">Isso pode ser resolvido executando com uma versão de lançamento desprotegida do executável do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="c0c27-637">Instalar o AppVerifier 4,0 (ou superior) em um computador que executa o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0c27-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="c0c27-638">Inicie o AppVerifier e clique em arquivo-> Adicionar aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0c27-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="c0c27-639">Localize o executável do jogo, selecione-o e clique em abrir</span><span class="sxs-lookup"><span data-stu-id="c0c27-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="c0c27-640">Na seção "aplicativos", selecione o executável do jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="c0c27-641">Selecione os seguintes testes na seção "Noções básicas":</span><span class="sxs-lookup"><span data-stu-id="c0c27-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="c0c27-642">Alças</span><span class="sxs-lookup"><span data-stu-id="c0c27-642">Handles</span></span>
    -   <span data-ttu-id="c0c27-643">Heaps</span><span class="sxs-lookup"><span data-stu-id="c0c27-643">Heaps</span></span>
    -   <span data-ttu-id="c0c27-644">Locks</span><span class="sxs-lookup"><span data-stu-id="c0c27-644">Locks</span></span>
    -   <span data-ttu-id="c0c27-645">Memória</span><span class="sxs-lookup"><span data-stu-id="c0c27-645">Memory</span></span>
    -   <span data-ttu-id="c0c27-646">TLS</span><span class="sxs-lookup"><span data-stu-id="c0c27-646">TLS</span></span>

6.  <span data-ttu-id="c0c27-647">Selecione os seguintes testes na seção "diversos":</span><span class="sxs-lookup"><span data-stu-id="c0c27-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="c0c27-648">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="c0c27-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="c0c27-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="c0c27-649">DirtyStacks</span></span>

7.  <span data-ttu-id="c0c27-650">Verifique se todos os outros testes não estão selecionados</span><span class="sxs-lookup"><span data-stu-id="c0c27-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="c0c27-651">Iniciar o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-651">Launch the game</span></span>
9.  <span data-ttu-id="c0c27-652">Jogue o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-652">Play the game</span></span>
10. <span data-ttu-id="c0c27-653">Fechar o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-653">Close the game</span></span>
11. <span data-ttu-id="c0c27-654">Em AppVerifier, selecione Exibir-> logs</span><span class="sxs-lookup"><span data-stu-id="c0c27-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="c0c27-655">Na seção "aplicativos", selecione o arquivo de .exe do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0c27-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="c0c27-656">Na seção "logs", selecione o arquivo de log e observe a contagem de erros.</span><span class="sxs-lookup"><span data-stu-id="c0c27-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="c0c27-657">Se não houver erros, encerre os testes do AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="c0c27-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="c0c27-658">Se houver erros, clique no botão exibir</span><span class="sxs-lookup"><span data-stu-id="c0c27-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="c0c27-659">Pesquisar o documento (CTRL + F) para severidade = "erro</span><span class="sxs-lookup"><span data-stu-id="c0c27-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="c0c27-660">Criar bugs com base na parte da Camadaname = da falha</span><span class="sxs-lookup"><span data-stu-id="c0c27-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="c0c27-661">Teste de manifesto 6,2-mt.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="c0c27-662">**Caso de teste: 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="c0c27-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="c0c27-663">Essa ferramenta é executada em um prompt de comando onde MT.exe está localizado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="c0c27-664">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="c0c27-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="c0c27-665">Clique em Iniciar-> executar-> digite cmd e clique no botão OK</span><span class="sxs-lookup"><span data-stu-id="c0c27-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="c0c27-666">Execute a ferramenta de mt.exe para gerar um arquivo. manifest para cada arquivo de .exe que é instalado com o jogo</span><span class="sxs-lookup"><span data-stu-id="c0c27-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="c0c27-667">Abrir o arquivo. manifest gerado</span><span class="sxs-lookup"><span data-stu-id="c0c27-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="c0c27-668">Certifique-se de que cada arquivo de .exe contém o seguinte (solicitado:</span><span class="sxs-lookup"><span data-stu-id="c0c27-668">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="c0c27-669">O nível de execução solicitado deve estar presente para cada arquivo e dpiAware deve estar presente para pelo menos o arquivo executável do jogo s.</span><span class="sxs-lookup"><span data-stu-id="c0c27-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="c0c27-670">6,3 de thread seqüestrador-threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="c0c27-671">Essa ferramenta é executada em um prompt de comando onde threadhijacker.exe está localizado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="c0c27-672">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="c0c27-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="c0c27-673">Em que Str é o nome \_ do \_program.exe</span><span class="sxs-lookup"><span data-stu-id="c0c27-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="c0c27-674">Ative o Gerenciador de tarefas, clique na guia processos e localize o nome do executável do jogo.</span><span class="sxs-lookup"><span data-stu-id="c0c27-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="c0c27-675">Abrir um prompt de comando no modo de administrador</span><span class="sxs-lookup"><span data-stu-id="c0c27-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="c0c27-676">Navegue até o diretório onde threadhijacker.exe está</span><span class="sxs-lookup"><span data-stu-id="c0c27-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="c0c27-677">Tipo: **threadhijacker.exe/Process:** Str, em que Str é o nome do executável que você deseja atingir</span><span class="sxs-lookup"><span data-stu-id="c0c27-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="c0c27-678">6,4 Microsoft Games para Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="c0c27-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="c0c27-679">Essa ferramenta está localizada no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="c0c27-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="c0c27-680">Depois que o SDK é instalado em um computador, o instalador da ferramenta de teste jogos para Windows pode ser colocado no computador de teste e instalado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="c0c27-681">Localize o instalador da ferramenta de teste do Microsoft Games para Windows no computador de desenvolvimento em que o SDK do DirectX está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="c0c27-682">Por padrão, ele é colocado no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="c0c27-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="c0c27-683">Copie o instalador (MicrosoftGFWTestTool.msi/setup.exe) para o computador de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="c0c27-684">Execute o instalador.</span><span class="sxs-lookup"><span data-stu-id="c0c27-684">Run the installer.</span></span>
3.  <span data-ttu-id="c0c27-685">Inicie a ferramenta de teste Microsoft Games para Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c27-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="c0c27-686">No campo **lista de projetos** , substitua **criar novo projeto** pelo nome do título e clique em **criar novo**.</span><span class="sxs-lookup"><span data-stu-id="c0c27-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="c0c27-687">Aguarde a conclusão da linha de base.</span><span class="sxs-lookup"><span data-stu-id="c0c27-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="c0c27-688">Preencha todas as informações que você possa ter na seção **informações do jogo** e clique em **Atualizar informações do jogo**.</span><span class="sxs-lookup"><span data-stu-id="c0c27-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="c0c27-689">Clique na guia **casos de teste** .</span><span class="sxs-lookup"><span data-stu-id="c0c27-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="c0c27-690">Começando na parte superior, prossiga com os casos de teste, clicando em **passar** ou **falhar** conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="c0c27-691">Consulte "escrevendo um bug", mais adiante nesta seção, para obter detalhes sobre como incluir um bug no relatório.</span><span class="sxs-lookup"><span data-stu-id="c0c27-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="c0c27-692">Retorne à guia **projetos** depois de revisar o relatório (marcando as guias **relatório** e **edição de bug** ).</span><span class="sxs-lookup"><span data-stu-id="c0c27-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="c0c27-693">Clique em **Compilar relatório**.</span><span class="sxs-lookup"><span data-stu-id="c0c27-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="c0c27-694">Uma janela será aberta quando o relatório terminar a compilação.</span><span class="sxs-lookup"><span data-stu-id="c0c27-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="c0c27-695">Aqui, você encontrará um .ZIP nome de arquivo *ProjectName* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="c0c27-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="c0c27-696">Esse arquivo contém todos os logs e resultados coletados durante a fase de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="c0c27-697">Escrevendo um bug</span><span class="sxs-lookup"><span data-stu-id="c0c27-697">Writing a Bug</span></span>

<span data-ttu-id="c0c27-698">Há duas maneiras de escrever um relatório de bugs: você pode percorrer os casos de teste e clicar em **falha** quando o título falha em um caso de teste, ou você pode clicar na guia **edição de bug** e adicionar manualmente um relatório de bug.</span><span class="sxs-lookup"><span data-stu-id="c0c27-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="c0c27-699">Clicando em falha em um caso de teste</span><span class="sxs-lookup"><span data-stu-id="c0c27-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="c0c27-700">Quando você clica em **falha** em um caso de teste, a lista suspensa **tipo de problema** será automaticamente definida como o tipo de caso de teste.</span><span class="sxs-lookup"><span data-stu-id="c0c27-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="c0c27-701">Adicione uma breve descrição ao **campo Título** que descreve brevemente o problema.</span><span class="sxs-lookup"><span data-stu-id="c0c27-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="c0c27-702">Adicione uma descrição detalhada do problema ao **campo Comportamento** Observado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="c0c27-703">Conforme apropriado, adicione o que era esperado (em vez de uma descrição do problema) ao **campo Comportamento** Esperado.</span><span class="sxs-lookup"><span data-stu-id="c0c27-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="c0c27-704">Adicione uma descrição detalhada de como reproduzir o problema no **campo Repro-Steps.**</span><span class="sxs-lookup"><span data-stu-id="c0c27-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="c0c27-705">Quando terminar, clique no **botão** Salvar.</span><span class="sxs-lookup"><span data-stu-id="c0c27-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="c0c27-706">Adicionando manualmente um bug</span><span class="sxs-lookup"><span data-stu-id="c0c27-706">Manually Adding a Bug</span></span>

<span data-ttu-id="c0c27-707">Esse processo é o mesmo que clicar em **Falhar**, com exceção da lista de listas listadas automaticamente populadas.</span><span class="sxs-lookup"><span data-stu-id="c0c27-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="c0c27-708">Nesse caso, selecione o tipo de falha TCR apropriado ou selecione Problema não **\* \* \* \* TR** para bugs que estão fora do intervalo de TR, mas ainda devem ser relatados.</span><span class="sxs-lookup"><span data-stu-id="c0c27-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="c0c27-709">Recursos</span><span class="sxs-lookup"><span data-stu-id="c0c27-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="c0c27-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Jogos para Windows: Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="c0c27-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="c0c27-711">Jogos para Requisitos Técnicos do Windows: Práticas recomendadas para jogos no Windows XP, Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0c27-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="c0c27-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="c0c27-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="c0c27-713">Windows SDKs</span><span class="sxs-lookup"><span data-stu-id="c0c27-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="c0c27-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Diretrizes de controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c0c27-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-715">[Requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c0c27-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer informações</span><span class="sxs-lookup"><span data-stu-id="c0c27-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="c0c27-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c0c27-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="c0c27-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Portal do Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="c0c27-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="c0c27-719">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="c0c27-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="c0c27-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Portal do Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="c0c27-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="c0c27-721">[Central de Desenvolvedores do DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c0c27-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="c0c27-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog do SDK de Jogos para Windows e DirectX</span><span class="sxs-lookup"><span data-stu-id="c0c27-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="c0c27-723">Jogos para Windows e SDK do DirectX</span><span class="sxs-lookup"><span data-stu-id="c0c27-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="c0c27-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artigos adicionais do DirectX</span><span class="sxs-lookup"><span data-stu-id="c0c27-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="c0c27-725">Artigos técnicos do DirectX</span><span class="sxs-lookup"><span data-stu-id="c0c27-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

