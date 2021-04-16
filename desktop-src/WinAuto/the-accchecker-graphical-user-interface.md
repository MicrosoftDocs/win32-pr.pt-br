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
# <a name="the-accchecker-graphical-user-interface"></a>A interface gráfica do usuário do AccChecker

Este tópico descreve os elementos que compõem a GUI do AccChecker.

-   [Guia de verificações](#verifications-tab)
-   [Guia resultados](#results-tab)
-   [Guias de leitor de tela MSAA e UIA](#msaa-and-uia-screen-reader-tabs)
-   [Guias de árvore MSAA e UIA](#msaa-and-uia-tree-tabs)
-   [Menu arquivo](#file-menu)
-   [Tópicos relacionados](#related-topics)

## <a name="verifications-tab"></a>Guia de verificações

AccChecker começa com a exibição padrão da guia **verificações** :

![Captura de tela que mostra a guia ' verificações ' no verificador de acessibilidade U.](images/accchecker-verifications-tab.png)

A guia **verificações** contém os componentes a seguir.

-   **Seletor de destino de verificação** Oferece as seguintes opções para selecionar um aplicativo ou controle de destino.
    -   Escolha um destino na lista suspensa preenchida previamente. Esta lista contém todos os HWNDs de nível superior identificados na inicialização.
    -   Escolha um HWND com base no local do cursor do mouse (os controles selecionáveis são realçados com um retângulo vermelho). Essa opção permite que você selecione qualquer objeto visível que tenha um HWND.
    -   Insira um HWND específico.
-   **Lista de verificação de rotinas de verificação** Fornece a capacidade de selecionar a rotina de verificação desejada a ser executada em um aplicativo ou controle. Consulte rotinas de verificação para obter mais informações.
-   **Seletor de arquivo de supressão de erro e aviso** Os arquivos de supressão são gerados na guia **resultados** da verificação. Clicando com o botão direito do mouse em uma mensagem de erro ou de aviso e selecionando **suprimir** no menu de contexto, um sinalizador é definido para essa mensagem. Se a caixa de seleção **supressões** estiver marcada, as entradas suprimidas aparecerão na lista. Uma entrada suprimida pode ser dessuprimida usando o mesmo menu de contexto usado para suprimir.

    Um arquivo de supressão é salvo em formato XML selecionando **salvar supressão** no menu **arquivo** . Esse arquivo é consumido em execuções de verificação subsequentes em que as mensagens serão ocultadas. Para remover o arquivo de supressão, clique em **limpar**. Para obter informações sobre mensagens específicas, consulte mensagens de log de verificação. Use **Salvar log** no menu **arquivo** para salvar a lista inteira como um arquivo de log em XML ou como um arquivo de texto formatado.

    ![Guia de resultados do accchecker com o item de contexto de supressão realçado](images/accchecker-results-tab-with-suppress.png)

    O exemplo a seguir mostra o conteúdo de um arquivo de supressão gerado pela execução das verificações de **Propriedades** no aplicativo do painel de controle do firewall do Windows. O erro com uma ID de "ElementHasNoName" foi escolhido para supressão neste exemplo.

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

    

-   **Mostrar resultados priorizados** Oferece as seguintes opções para filtrar os resultados da verificação por prioridade.
    -   **Todos** Incluir todos os resultados, independentemente da prioridade.
    -   **Apenas P1** Inclua apenas os resultados de prioridade 0 e prioridade 1.
    -   **Apenas P1 P2** Inclua a prioridade 0 a resultados de prioridade 2.
-   **Executar verificações selecionadas** Fornece o botão **executar verificações** para iniciar o processo de verificação. Enquanto as verificações estão em execução, o botão é alterado para **cancelar as verificações** e pode ser usado para interromper as verificações após a conclusão da atual.

## <a name="results-tab"></a>Guia resultados

A guia **resultados** é preenchida depois que as tarefas de verificação selecionadas são concluídas. Ele consiste nos seguintes componentes.

-   A lista de mensagens, que exibe o erro, o aviso e as mensagens informativas geradas pelas tarefas de verificação selecionadas. As mensagens exibidas podem ser filtradas por tipo usando as caixas de seleção acima da lista de mensagens.
-   Os detalhes da mensagem e uma captura de tela do destino de verificação. A seleção de uma mensagem na lista de mensagens exibe mais detalhes e realça o elemento correspondente no painel captura de tela. O botão **Visualizar** , alterna AccChecker para a guia de **árvore MSAA** . Se um erro for realçado na guia **resultados** , o elemento correspondente será realçado na guia de **árvore MSAA** .

Clicar com o botão direito do mouse em uma mensagem expõe um menu de contexto com os itens a seguir.

-   **Suprimir** Adiciona a mensagem à lista de supressão.
-   **Copiar para área de transferência** Copia os detalhes da mensagem para a área de transferência.
-   **Visualizar** Alterna AccChecker para a guia de **árvore MSAA** . O elemento que corresponde ao erro selecionado é realçado.
-   **Ajuda** do Exibe informações adicionais sobre a mensagem.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Guias de leitor de tela MSAA e UIA

As guias leitor de tela MSAA e leitor de tela UIA são semelhantes. Ambos exibem uma transcrição dos elementos encontrados em uma passagem simulada do destino de verificação por um leitor de tela, exceto que ele mostra a implementação de MSAA e o outro mostra a implementação de UIA.

Os elementos são navegados e registrados assim como um leitor de tela os lêem. As informações apresentadas nesta guia são essenciais para confirmar que apenas informações úteis e relevantes estão sendo anunciadas. Por exemplo, um nome de controle de som normal, como "edição MenuItem" ou "fechamento de pressão", é aceitável; no entanto, um nome de controle que não faz sentido, como "CPNavPanel22" ou "defaultvalue1", não é aceitável. O botão **Visualizar** faz com que AccChecker alterne para a **árvore MSAA** ou a guia de **árvore UIA** . Se um elemento for realçado na guia **leitor de tela** , o elemento correspondente será realçado na **árvore MSAA** ou na guia de **árvore UIA** .

A rotina de verificação **ScreenReader** em **consistente** deve ser selecionada na guia **verificações** para que a **guia leitor de tela MSAA** seja exibida. Da mesma forma, a rotina de verificação de **UiaScreenReader** deve ser selecionada para que a guia do **leitor de tela UIA** seja exibida.

A captura de tela a seguir mostra a guia leitor de tela UIA com um exemplo de verificação do bloco de notas.

![guia leitor de tela do accchecker exibindo resultados da verificação de exemplo](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Guias de árvore MSAA e UIA

Executar qualquer rotina de verificação faz com que o AccChecker compile todos os elementos visíveis no destino de verificação e os exiba hierarquicamente na guia de **árvore MSAA** e na guia de **árvore UIA** . A captura de tela a seguir mostra a guia de árvore MSAA com a hierarquia de elementos para o bloco de notas.

![Guia de árvore de MSAA accchecker](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menu Arquivo



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menu</th>
<th>Comando</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><strong>Arquivo</strong>$ {remove} $<br />
</td>
<td><strong>Abrir</strong></td>
<td>Fornece as opções a seguir.<br/>
<ul>
<li><strong>Dll de verificações</strong> Abre uma DLL de verificação. As verificações de AccChecker nativas são encapsuladas em uma DLL autônoma (VerificationRoutines.dll). Esse design permite que as equipes de teste criem seu próprio conjunto de verificações com base na plataforma de interface do usuário que está sendo testada.</li>
<li><strong>Arquivo de log</strong> Permite que você escolha um arquivo de log de verificação para abrir.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Carregar automaticamente as verificações disponíveis</strong></td>
<td>Carrega automaticamente todas as verificações de AccChecker disponíveis.</td>

</tr>
<tr class="odd">
<td><strong>Salvar log</strong></td>
<td>Salve o log de verificação como XML ou como texto sem formatação. O texto sem formatação é mais legível.</td>

</tr>
<tr class="even">
<td><strong>Salvar supressão</strong></td>
<td>Salve o log de supressão como XML. Esse arquivo especifica as mensagens de verificação a serem ignoradas no teste de regressão.</td>

</tr>
<tr class="odd">
<td><strong>Sair</strong></td>
<td>Fecha a ferramenta AccChecker.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Verificações</strong>$ {remove} $<br />
</td>
<td><strong>Executar agora</strong></td>
<td>Execute as rotinas de verificação conforme especificado para o destino de verificação escolhido.</td>
</tr>
<tr class="odd">
<td><strong>Habilitar tudo</strong></td>
<td>Marque todas as caixas de seleção de rotina de verificação.</td>

</tr>
<tr class="even">
<td><strong>Desabilitar tudo</strong></td>
<td>Desmarque todas as caixas de seleção de rotina de verificação.</td>

</tr>
<tr class="odd">
<td><strong>Opções</strong></td>
<td><strong>Always On superior</strong></td>
<td>Tornar AccChecker a janela superior na ordem z.</td>
</tr>
<tr class="even">
<td rowspan="2"><strong>Ajuda</strong>$ {remove} $<br />
</td>
<td><strong>Ajuda</strong></td>
<td>Exibir informações de ajuda.</td>
</tr>
<tr class="odd">
<td><strong>Sobre</strong></td>
<td>Exiba a versão do AccChecker e um endereço de email para entrar em contato com a Microsoft sobre o AccChecker.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





