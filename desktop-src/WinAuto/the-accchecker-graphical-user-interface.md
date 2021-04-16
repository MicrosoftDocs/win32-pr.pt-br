---
title: A interface gráfica do usuário do AccChecker
description: Este tópico descreve os elementos que compõem a GUI do AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104557949"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="8f5ff-103">A interface gráfica do usuário do AccChecker</span><span class="sxs-lookup"><span data-stu-id="8f5ff-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="8f5ff-104">Este tópico descreve os elementos que compõem a GUI do AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="8f5ff-105">Guia de verificações</span><span class="sxs-lookup"><span data-stu-id="8f5ff-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="8f5ff-106">Guia resultados</span><span class="sxs-lookup"><span data-stu-id="8f5ff-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="8f5ff-107">Guias de leitor de tela MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="8f5ff-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="8f5ff-108">Guias de árvore MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="8f5ff-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="8f5ff-109">Menu arquivo</span><span class="sxs-lookup"><span data-stu-id="8f5ff-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="8f5ff-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f5ff-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="8f5ff-111">Guia de verificações</span><span class="sxs-lookup"><span data-stu-id="8f5ff-111">Verifications Tab</span></span>

<span data-ttu-id="8f5ff-112">AccChecker começa com a exibição padrão da guia **verificações** :</span><span class="sxs-lookup"><span data-stu-id="8f5ff-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Captura de tela que mostra a guia ' verificações ' no verificador de acessibilidade U.](images/accchecker-verifications-tab.png)

<span data-ttu-id="8f5ff-114">A guia **verificações** contém os componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="8f5ff-115">**Seletor de destino de verificação** Oferece as seguintes opções para selecionar um aplicativo ou controle de destino.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="8f5ff-116">Escolha um destino na lista suspensa preenchida previamente.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="8f5ff-117">Esta lista contém todos os HWNDs de nível superior identificados na inicialização.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="8f5ff-118">Escolha um HWND com base no local do cursor do mouse (os controles selecionáveis são realçados com um retângulo vermelho).</span><span class="sxs-lookup"><span data-stu-id="8f5ff-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="8f5ff-119">Essa opção permite que você selecione qualquer objeto visível que tenha um HWND.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="8f5ff-120">Insira um HWND específico.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="8f5ff-121">**Lista de verificação de rotinas de verificação** Fornece a capacidade de selecionar a rotina de verificação desejada a ser executada em um aplicativo ou controle.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="8f5ff-122">Consulte rotinas de verificação para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="8f5ff-123">**Seletor de arquivo de supressão de erro e aviso** Os arquivos de supressão são gerados na guia **resultados** da verificação. Clicando com o botão direito do mouse em uma mensagem de erro ou de aviso e selecionando **suprimir** no menu de contexto, um sinalizador é definido para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="8f5ff-124">Se a caixa de seleção **supressões** estiver marcada, as entradas suprimidas aparecerão na lista.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="8f5ff-125">Uma entrada suprimida pode ser dessuprimida usando o mesmo menu de contexto usado para suprimir.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="8f5ff-126">Um arquivo de supressão é salvo em formato XML selecionando **salvar supressão** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="8f5ff-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="8f5ff-127">Esse arquivo é consumido em execuções de verificação subsequentes em que as mensagens serão ocultadas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="8f5ff-128">Para remover o arquivo de supressão, clique em **limpar**.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="8f5ff-129">Para obter informações sobre mensagens específicas, consulte mensagens de log de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="8f5ff-130">Use **Salvar log** no menu **arquivo** para salvar a lista inteira como um arquivo de log em XML ou como um arquivo de texto formatado.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![Guia de resultados do accchecker com o item de contexto de supressão realçado](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="8f5ff-132">O exemplo a seguir mostra o conteúdo de um arquivo de supressão gerado pela execução das verificações de **Propriedades** no aplicativo do painel de controle do firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="8f5ff-133">O erro com uma ID de "ElementHasNoName" foi escolhido para supressão neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="8f5ff-134">**Mostrar resultados priorizados** Oferece as seguintes opções para filtrar os resultados da verificação por prioridade.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="8f5ff-135">**Todos** Incluir todos os resultados, independentemente da prioridade.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="8f5ff-136">**Apenas P1** Inclua apenas os resultados de prioridade 0 e prioridade 1.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="8f5ff-137">**Apenas P1 P2** Inclua a prioridade 0 a resultados de prioridade 2.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="8f5ff-138">**Executar verificações selecionadas** Fornece o botão **executar verificações** para iniciar o processo de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="8f5ff-139">Enquanto as verificações estão em execução, o botão é alterado para **cancelar as verificações** e pode ser usado para interromper as verificações após a conclusão da atual.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="8f5ff-140">Guia resultados</span><span class="sxs-lookup"><span data-stu-id="8f5ff-140">Results Tab</span></span>

<span data-ttu-id="8f5ff-141">A guia **resultados** é preenchida depois que as tarefas de verificação selecionadas são concluídas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="8f5ff-142">Ele consiste nos seguintes componentes.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-142">It consists of the following components.</span></span>

-   <span data-ttu-id="8f5ff-143">A lista de mensagens, que exibe o erro, o aviso e as mensagens informativas geradas pelas tarefas de verificação selecionadas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="8f5ff-144">As mensagens exibidas podem ser filtradas por tipo usando as caixas de seleção acima da lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="8f5ff-145">Os detalhes da mensagem e uma captura de tela do destino de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="8f5ff-146">A seleção de uma mensagem na lista de mensagens exibe mais detalhes e realça o elemento correspondente no painel captura de tela.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="8f5ff-147">O botão **Visualizar** , alterna AccChecker para a guia de **árvore MSAA** . Se um erro for realçado na guia **resultados** , o elemento correspondente será realçado na guia de **árvore MSAA** .</span><span class="sxs-lookup"><span data-stu-id="8f5ff-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="8f5ff-148">Clicar com o botão direito do mouse em uma mensagem expõe um menu de contexto com os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="8f5ff-149">**Suprimir** Adiciona a mensagem à lista de supressão.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="8f5ff-150">**Copiar para área de transferência** Copia os detalhes da mensagem para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="8f5ff-151">**Visualizar** Alterna AccChecker para a guia de **árvore MSAA** . O elemento que corresponde ao erro selecionado é realçado.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="8f5ff-152">**Ajuda** do Exibe informações adicionais sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="8f5ff-153">Guias de leitor de tela MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="8f5ff-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="8f5ff-154">As guias leitor de tela MSAA e leitor de tela UIA são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="8f5ff-155">Ambos exibem uma transcrição dos elementos encontrados em uma passagem simulada do destino de verificação por um leitor de tela, exceto que ele mostra a implementação de MSAA e o outro mostra a implementação de UIA.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="8f5ff-156">Os elementos são navegados e registrados assim como um leitor de tela os lêem.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="8f5ff-157">As informações apresentadas nesta guia são essenciais para confirmar que apenas informações úteis e relevantes estão sendo anunciadas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="8f5ff-158">Por exemplo, um nome de controle de som normal, como "edição MenuItem" ou "fechamento de pressão", é aceitável; no entanto, um nome de controle que não faz sentido, como "CPNavPanel22" ou "defaultvalue1", não é aceitável.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="8f5ff-159">O botão **Visualizar** faz com que AccChecker alterne para a **árvore MSAA** ou a guia de **árvore UIA** . Se um elemento for realçado na guia **leitor de tela** , o elemento correspondente será realçado na **árvore MSAA** ou na guia de **árvore UIA** .</span><span class="sxs-lookup"><span data-stu-id="8f5ff-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="8f5ff-160">A rotina de verificação **ScreenReader** em **consistente** deve ser selecionada na guia **verificações** para que a **guia leitor de tela MSAA** seja exibida.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="8f5ff-161">Da mesma forma, a rotina de verificação de **UiaScreenReader** deve ser selecionada para que a guia do **leitor de tela UIA** seja exibida.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="8f5ff-162">A captura de tela a seguir mostra a guia leitor de tela UIA com um exemplo de verificação do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![guia leitor de tela do accchecker exibindo resultados da verificação de exemplo](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="8f5ff-164">Guias de árvore MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="8f5ff-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="8f5ff-165">Executar qualquer rotina de verificação faz com que o AccChecker compile todos os elementos visíveis no destino de verificação e os exiba hierarquicamente na guia de **árvore MSAA** e na guia de **árvore UIA** . A captura de tela a seguir mostra a guia de árvore MSAA com a hierarquia de elementos para o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![Guia de árvore de MSAA accchecker](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="8f5ff-167">Menu Arquivo</span><span class="sxs-lookup"><span data-stu-id="8f5ff-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f5ff-168">Menu</span><span class="sxs-lookup"><span data-stu-id="8f5ff-168">Menu</span></span></th>
<th><span data-ttu-id="8f5ff-169">Comando</span><span class="sxs-lookup"><span data-stu-id="8f5ff-169">Command</span></span></th>
<th><span data-ttu-id="8f5ff-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5ff-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="8f5ff-171"><strong>Arquivo</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="8f5ff-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8f5ff-172"><strong>Abrir</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="8f5ff-173">Fornece as opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="8f5ff-174"><strong>Dll de verificações</strong> Abre uma DLL de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="8f5ff-175">As verificações de AccChecker nativas são encapsuladas em uma DLL autônoma (VerificationRoutines.dll).</span><span class="sxs-lookup"><span data-stu-id="8f5ff-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="8f5ff-176">Esse design permite que as equipes de teste criem seu próprio conjunto de verificações com base na plataforma de interface do usuário que está sendo testada.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="8f5ff-177"><strong>Arquivo de log</strong> Permite que você escolha um arquivo de log de verificação para abrir.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f5ff-178"><strong>Carregar automaticamente as verificações disponíveis</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="8f5ff-179">Carrega automaticamente todas as verificações de AccChecker disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8f5ff-180"><strong>Salvar log</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="8f5ff-181">Salve o log de verificação como XML ou como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="8f5ff-182">O texto sem formatação é mais legível.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8f5ff-183"><strong>Salvar supressão</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="8f5ff-184">Salve o log de supressão como XML.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-184">Save the suppression log as XML.</span></span> <span data-ttu-id="8f5ff-185">Esse arquivo especifica as mensagens de verificação a serem ignoradas no teste de regressão.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8f5ff-186"><strong>Sair</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="8f5ff-187">Fecha a ferramenta AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="8f5ff-188"><strong>Verificações</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="8f5ff-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8f5ff-189"><strong>Executar agora</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="8f5ff-190">Execute as rotinas de verificação conforme especificado para o destino de verificação escolhido.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f5ff-191"><strong>Habilitar tudo</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="8f5ff-192">Marque todas as caixas de seleção de rotina de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8f5ff-193"><strong>Desabilitar tudo</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="8f5ff-194">Desmarque todas as caixas de seleção de rotina de verificação.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8f5ff-195"><strong>Opções</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="8f5ff-196"><strong>Always On superior</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="8f5ff-197">Tornar AccChecker a janela superior na ordem z.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="8f5ff-198"><strong>Ajuda</strong>$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="8f5ff-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8f5ff-199"><strong>Ajuda</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="8f5ff-200">Exibir informações de ajuda.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f5ff-201"><strong>Sobre</strong></span><span class="sxs-lookup"><span data-stu-id="8f5ff-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="8f5ff-202">Exiba a versão do AccChecker e um endereço de email para entrar em contato com a Microsoft sobre o AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8f5ff-203">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f5ff-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5ff-204">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="8f5ff-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





