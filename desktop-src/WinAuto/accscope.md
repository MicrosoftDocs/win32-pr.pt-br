---
title: Ferramentas de acessibilidade – AccScope
description: A ferramenta AccScope permite que desenvolvedores e testadores avaliem a acessibilidade de seu aplicativo durante o desenvolvimento e o design do aplicativo, em vez de nas fases de teste tardias do ciclo de desenvolvimento de um aplicativo.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e55aa40822b786ee69185abe753bb0bacd65345d042526a126b4c8343a2639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327713"
---
# <a name="accessibility-tools---accscope"></a>Ferramentas de acessibilidade – AccScope

A **ferramenta AccScope** permite que desenvolvedores e testadores avaliem a acessibilidade de seu aplicativo durante o desenvolvimento e o design do aplicativo, em vez de nas fases de teste tardias do ciclo de desenvolvimento de um aplicativo. O teste pode até mesmo começar em fases de protótipo inicial. **O AccScope** pode visualizar como um leitor de tela expõe as informações de Automação da Interface do Usuário que um aplicativo fornece e pode mostrar áreas em que talvez você queira adicionar informações ou suporte ao seu aplicativo para melhorar sua acessibilidade.

> [!NOTE]
> **O AccScope** é uma ferramenta herdado. Em vez disso, [recomendamos o uso Insights](https://accessibilityinsights.io/) acessibilidade.

## <a name="about-accscope"></a>Sobre o AccScope

**O AccScope** é instalado com o Windows SDK (Software Development Kit). Ele está localizado na pasta \\ \\ < AccScope da plataforma *de versão* > \\ <  > \\ bin do caminho de instalação do SDK. Execute o programa AccScope.exe.

**O AccScope** é um aplicativo da área de trabalho, não um Windows Store. Você pode usá-lo para ver qualquer aplicativo que aparece como uma janela, incluindo um aplicativo da área de trabalho ou um aplicativo Windows Store.

Talvez seja necessário executar **o AccScope** como administrador na primeira vez que usá-lo, para habilitar o modo narrador.

**O AccScope** está disponível como parte dos binários das ferramentas de acessibilidade, no SDK do Windows. Ele não é distribuído como um download exe separado e não existe em SDKs anteriores.

## <a name="file-menu-options"></a>Opções do menu Arquivo

- Selecione **Atualizar** para atualizar todas as informações **no AccScope** para corresponder ao estado atual da janela de destino. Para uma interface do usuário que contém um grande número de elementos, isso pode levar vários segundos para ser concluído.
- Marque ou **desmarque Always On Top** para alterar o comportamento de janela da interface do usuário do **AccScope.** **Always On Top** marcado é o padrão.
- Selecione **Sair** para sair **do AccScope.**

## <a name="view-options"></a>Opções de exibição

- Selecione **Tela Inteira** para executar a ferramenta **AccScope** em uma exibição de tela inteira (em seguida, use a tabulação para exibir a janela de destino). Se **o AccScope** e o aplicativo de destino estão executando tela inteira, posicionamento, retângulos delimitadores e visualização geral de elementos corresponderão entre o aplicativo e a exibição **do AccScope.**
    > [!Note]  
    > **AccScope** e seu destino devem ser executados na mesma exibição.

     

- Selecione **Foco Automático para** permitir que o AccScope altere a janela de destino sempre que um usuário mover o foco para a janela (usando o mouse ou o teclado).
- Selecione **Atualização Automática** para habilitar o modo **AccScope** que atualiza todos os dados de acessibilidade da janela de destino a cada 5 segundos. Isso será útil se os dados de Automação da Interface do Usuário da janela de destino mudarem constantemente.
- Selecione **Regiões ao Vivo** para realçar todas as regiões ao vivo que emem notificações na janela de destino. Um evento de região ao vivo acionando exibe um pop-up vermelho que tem informações sobre a região ao vivo, incluindo seu nome e seu valor "aria-live" (ou o valor equivalente de ARIA análogo para aplicativos que não usam diretamente HTML, mas usando o conceito de Regiões Ao Vivo no suporte do Automação da Interface do Usuário).

## <a name="element-mode"></a>Modo de elemento

Você pode optar por exibir uma janela de destino por meio de um destes modos:

- **Controle Folha**: mostra uma Automação da Interface do Usuário  de elementos Control com relações pai-filho, ou seja, uma exibição de controles interativos de "nível folha". Use essa opção para ver se todos os controles interativos estão aparecendo corretamente na árvore Automação da Interface do Usuário para uma **exibição controle.**
- **Padrão de** Texto: mostra intervalos de texto visíveis dos **contêineres TextPattern** da janela de destino. Use essa opção para representar visualmente os intervalos de texto visíveis Automação da Interface do Usuário **elementos TextPattern.**
- **Narrador:** mostra os elementos Automação da Interface do Usuário que o Narrador pode identificar usando a metáfora "navegação de item" do Narrador.
- **Filtro Personalizado:** mostra uma árvore de controle filtrada com uma opção de subconjunto de controle: **Botão** **,** Caixa de seleção , **Caixa** de combinação , **Grade**, **Hiperlink**, **Lista**, **Menu** **ou Tabela**.

Alterar a **configuração modo** de elemento dispara uma atualização da visualização. Para uma interface do usuário que contém um grande número de elementos, isso pode levar vários segundos para ser concluído.

## <a name="layout-options"></a>Opções de layout

Você pode selecionar **Visual** ou **Listar como** o modo de visualização para o layout **do AccScope.** **O visual** coloca os elementos no espaço de coordenadas na mesma relação que a janela de destino. **A** lista ordena os elementos em uma lista decrescente alinhada à esquerda na janela **AccScope** e a ordem de lista é equivalente à ordem de tabulação ou à ordem de leitura.

- Selecione uma  opção em Mostrar Imagens para controlar quando os retângulos simples para elementos de imagem são substituídos pela imagem real (ou um pequeno viewport dessa imagem, pois geralmente os retângulos são menores do que a imagem real). O padrão é **Em Foco,** que exibe a imagem quando você navega dentro de **AccScope** e passe o mouse sobre o retângulo para um elemento de imagem. As opções alternativas são **Sempre** ou **Nunca.**
- Selecione **Mostrar Dica de** Ferramenta para mostrar informações básicas do elemento sempre que passar o mouse sobre um elemento na **visualização do AccScope.** Se o **Modo de**  Elemento for **Controle Folha** ou Padrão de Texto, as informações mostradas na dica de ferramenta serão as propriedades de nível de elemento de Automação da Interface do Usuário prioridade mais alta. Se o **Modo de Elemento** for **Narrador,** as informações incluirão o texto que o Narrador leria para o elemento.
- Selecione **Mostrar Números para** exibir números de sequência que indicam a ordem de renderização do controle no layout. O esquema de número baseia-se na **configuração Modo de** Elemento:
    - **Controle Folha**: os números indicam a ordem na qual os controles folha aparecem na árvore Automação da Interface do Usuário dados.
    - **Padrão de** Texto: os números indicam a ordem na qual os intervalos de texto aparecem em um intervalo de documentos.
    - **Narrador:** o número indica a ordem na qual os elementos são navegados na navegação de item do Narrador.

## <a name="choosing-a-window"></a>Escolhendo uma janela

No rótulo **Janela,** você encontrará um menu suspenso que lista todas as janelas HWND que estão ativas no sistema no momento. O texto de cada janela que aparece na lista suspenso é o título da janela e também uma ID de janela hexaxa entre colchetes. Escolha um deles para alterar a janela de destino na **qual o AccScope** está relatando. Você pode escolher o mesmo item novamente para obter o mesmo comportamento de uma Atualização **explícita.**

## <a name="using-the-accscope-visualization"></a>Usando a visualização do AccScope

A imagem abaixo é uma captura de tela da **visualização do AccScope.** Esta captura de tela específica mostra a ferramenta **AccScope** exibindo a janela de nível superior para a saída de exemplo de acessibilidade [XAML,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) em execução como um aplicativo no mesmo computador. Esta captura de tela mostra o modo de elemento padrão do **Controle Folha** e o **valor visual** para **Layout**.

![Captura de tela da visualização do AccScope](images/accscopescreenshot.png)

Observe como essa visualização representa os controles no espaço de coordenada aproximado que você verá no aplicativo. Mas, em vez de mostrar os visuais XAML ou o  texto completo dos controles de texto, ele mostra os valores da propriedade Name que vêm de cada elemento de controle, usando Automação da Interface do Usuário.

Além das opções de menu descritas anteriormente, você também pode usar estas técnicas:

- Clique no retângulo de qualquer elemento nas **visualizações Visual** ou **Lista** para exibir um pop-up Propriedades da **UIA.** Isso lista várias propriedades Automação da Interface do Usuário importantes para esse elemento, incluindo algumas das propriedades [**padrão IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) e outras informações, como valores ARIA e uma descrição do **provedor**.
- Clique com o botão direito do mouse  no retângulo de qualquer elemento nas visualizações **Visual** ou Lista para exibir um menu de contexto para praticar os padrões que o elemento dá suporte. Por exemplo, se um elemento dá suporte a [**InvokePattern,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)o menu de contexto inclui um item para **Invocar**. Selecione esse item e a API de padrão apropriada é usada no aplicativo correspondente. **O AccScope** dá suporte a esse recurso para os seguintes padrões: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem,** **ScrollItem**.
- Ajuste o **controle deslizante** Transparência para alterar a opacidade/transparência da janela **AccScope.** Por padrão, ele é mostrado como 100% de opacidade. Tornar a janela parcialmente transparente pode ser útil para ver as partes da janela de destino por meio da interface do usuário **do AccScope** ao usar o **Always On** Superior.
- Se elas são mostradas, use as barras de rolagem horizontais e verticais para alterar o centro de exibição da visualização. Isso será útil se você estiver usando a  opção layout **visual,** mas não estiver usando a opção exibição de Tela Inteira, deixando a janela **AccScope** pequena em comparação com a janela de destino.

## <a name="testing-the-narrator-scenario"></a>Testando o cenário do Narrador

O cenário do Narrador é o aspecto mais importante a ser testado ao usar **o AccScope,** que foi projetado especificamente para visualizar como a navegação básica de item do Narrador funciona quando ela é aplicada ao seu aplicativo.

Para testar o cenário do Narrador, use estas **opções de configuração do AccScope:**

- **Modo de elemento**: **Narrador**
- **Layout:** **Visual**
- **Opções** de layout: **Mostrar Dica de Ferramenta** e Mostrar Números **selecionados**

Aqui estão algumas áreas específicas do seu aplicativo para testar o cenário do Narrador:

- **Ordem do elemento:** Verifique se a ordem na qual o Narrador lê seus controles é precisa, de acordo com os números (círculos verdes) exibidos nas visualizações. Se os elementos não estão na ordem esperada para leitura, modifique a estrutura de interface do usuário do aplicativo e a árvore Automação da Interface do Usuário resultante e teste novamente até verificar se os elementos estão na ordem de leitura esperada.
- **Texto falado:** Mova o mouse dentro da visualização e passe o mouse sobre cada um dos retângulos de elemento para exibir as dicas de ferramenta para cada elemento. No modo Narrador, as dicas de ferramenta exibem uma entrada **de Texto do Narrador** que é literalmente o texto que o Narrador lê. Geralmente, esse texto é composto pelo **Nome e** pelo Tipo **de Controle**. Verifique se essas são as informações corretas para cada controle em sua interface do usuário. Se alguma informação estiver incorreta, modifique as Automação da Interface do Usuário por meio das técnicas habilitadas por sua estrutura de interface do usuário específica para fazer isso. (Se **o Tipo de** Controle for inesperado, talvez seja necessário usar um controle diferente, pois isso geralmente é controlado exclusivamente pelas implementações de controle de uma estrutura de interface do usuário.) Em seguida, teste novamente e verifique se **o Texto do Narrador** está correto.
- **Layout do elemento:** Verifique cada um desses casos:
    - Verifique se os elementos redundantes não são expostos pelo Narrador. Um exemplo de um elemento redundante é o controle de classificações em cada Windows item de peça da Store.
    - Verifique se os elementos importantes (elementos que o usuário precisa para realizar as principais tarefas no aplicativo) aparecem na navegação de item do Narrador.
    - Se você estiver usando o **layout** **visual** e um elemento estiver ausente porque os controles se sobrepõem, alternar para Layout de lista para ver a sequência relatada pelo Narrador.
    - Verifique se a estrutura Automação da Interface do Usuário árvore geral é precisa e esperada para seu aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Ferramentas de teste](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Verificação da Automação da Interface do Usuário](ui-automation-verify.md)
- [Acessibilidade da Microsoft](https://www.microsoft.com/accessibility/)
