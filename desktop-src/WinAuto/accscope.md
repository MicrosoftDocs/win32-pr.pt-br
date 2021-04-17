---
title: Ferramentas de acessibilidade – AccScope
description: A ferramenta AccScope permite que os desenvolvedores e testadores avaliem a acessibilidade de seus aplicativos durante o desenvolvimento e o design do aplicativo, em vez das fases de teste posteriores do ciclo de desenvolvimento de um aplicativo.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d057e818a0fe01ef6f219f1a03d82190d21ac14
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2020
ms.locfileid: "104570968"
---
# <a name="accessibility-tools---accscope"></a>Ferramentas de acessibilidade – AccScope

A ferramenta **AccScope** permite que os desenvolvedores e testadores avaliem a acessibilidade de seus aplicativos durante o desenvolvimento e o design do aplicativo, em vez das fases de teste posteriores do ciclo de desenvolvimento de um aplicativo. Os testes podem até mesmo começar nas fases do protótipo inicial. O **AccScope** pode visualizar como um leitor de tela expõe as informações de automação da interface do usuário que um aplicativo fornece e pode mostrar áreas em que você talvez queira adicionar informações ou suporte ao seu aplicativo para melhorar sua acessibilidade.

> [!NOTE]
> **AccScope** é uma ferramenta herdada. Em vez disso, recomendamos o uso de [informações de acessibilidade](https://accessibilityinsights.io/) .

## <a name="about-accscope"></a>Sobre o AccScope

O **AccScope** é instalado com o SDK (Software Development Kit) do Windows. Ele está localizado na \\ pasta bin \\ < *version* > \\ <  > \\ AccScope do caminho de instalação do SDK. Execute o programa AccScope.exe.

**AccScope** é um aplicativo de área de trabalho, não um aplicativo da Windows Store. Você pode usá-lo para examinar qualquer aplicativo que aparece como uma janela, incluindo um aplicativo de área de trabalho ou um aplicativo da Windows Store.

Talvez seja necessário executar **AccScope** como administrador na primeira vez que você usá-lo, para habilitar o modo do narrador.

O **AccScope** está disponível como parte dos binários das ferramentas de acessibilidade, na SDK do Windows. Ele não é distribuído como um download de exe separado e não existe em SDKs anteriores.

## <a name="file-menu-options"></a>Opções de menu arquivo

- Selecione **Atualizar** para atualizar todas as informações em **AccScope** para corresponder ao estado atual da janela de destino. Para uma interface do usuário que contém um grande número de elementos, isso pode levar vários segundos para ser concluído.
- Marque ou desmarque a seleção **sempre visível** para alterar o comportamento de janelas da interface do usuário do **amAccScope** . A opção **AlwaysOn sempre visível** é o padrão.
- Selecione **sair** para sair do **AccScope**.

## <a name="view-options"></a>Opções de exibição

- Selecione **tela inteira** para executar a ferramenta **AccScope** em uma exibição de tela inteira (em seguida, use Tab para exibir a janela de destino). Se **AccScope** e o aplicativo de destino estiverem executando tela inteira, posicionamento, retângulos delimitadores e a visualização geral dos elementos corresponderão entre seu aplicativo e a exibição **AccScope** .
    > [!Note]  
    > **AccScope** e seu destino devem ser executados na mesma exibição.

     

- Selecione **foco automático** para permitir que o AccScope altere a janela de destino sempre que um usuário mover o foco para a janela (usando o mouse ou o teclado).
- Selecione **atualização automática** para habilitar o modo **AccScope** que atualiza todos os dados de acessibilidade da janela de destino a cada 5 segundos. Isso será útil se os dados da automação da interface do usuário da Microsoft forem alterados constantemente.
- Selecione **regiões dinâmicas** para realçar todas as regiões dinâmicas que emitem notificações na janela de destino. Um acionamento de eventos de região ao vivo exibe um popup vermelho que tem informações sobre a região ao vivo, incluindo seu nome e seu valor de "Aria-Live" (ou o valor equivalente do ARIA analógico para aplicativos que não usam o HTML diretamente, mas usando o conceito de regiões dinâmicas no suporte de automação da interface do usuário).

## <a name="element-mode"></a>Modo de elemento

Você pode optar por exibir uma janela de destino por meio de um destes modos:

- **Controle folha**: mostra uma exibição de automação da interface do usuário de elementos de **controle** com relações pai-filho, em outras palavras, uma exibição de controles interativos de "nível de folha". Use esta opção para ver se todos os controles interativos estão aparecendo corretamente na árvore de automação da interface do usuário para um modo de exibição de **controle** .
- **Padrão de texto**: mostra os intervalos de texto visíveis dos contêineres de **TextPattern** da janela de destino. Use esta opção para representar visualmente os intervalos de texto visíveis dos elementos de **TextPattern** da automação da interface do usuário.
- **Narrador**: mostra os elementos de automação da interface do usuário que o Narrator pode identificar usando a metáfora de "item de navegação" do Narrator.
- **Filtro personalizado**: mostra uma árvore de controle filtrada com uma opção de subconjuntos de controle: **botão**, **caixa de seleção**, **ComboBox**, **grade**, **hiperlink**, **lista**, **menu** ou **tabela**.

A alteração da configuração de **modo de elemento** dispara uma atualização da visualização. Para uma interface do usuário que contém um grande número de elementos, isso pode levar vários segundos para ser concluído.

## <a name="layout-options"></a>Opções de layout

Você pode selecionar **Visual** ou **list** como o modo de visualização para o layout **AccScope** . O **Visual** coloca os elementos no espaço de coordenadas na mesma relação que a janela de destino. **List** ordena os elementos em uma lista decrescente que está alinhada à esquerda na janela **AccScope** e a ordem da lista é equivalente à ordem de tabulação ou à ordem de leitura.

- Selecione uma opção de **mostrar imagens** para controlar quando os retângulos simples para elementos de imagem são substituídos pela imagem real (ou um visor pequeno dessa imagem, pois geralmente os retângulos são menores do que a imagem real). O padrão é **focalizado**, que exibe a imagem quando você navega dentro de **AccScope** e passa o mouse sobre o retângulo de um elemento Image. As opções alternativas são **sempre** ou **nunca**.
- Selecione **Mostrar dica de ferramenta** para mostrar informações básicas sobre o elemento sempre que você passar o mouse sobre um elemento na visualização **AccScope** . Se o **modo de elemento** for **controle folha** ou **padrão de texto** , as informações mostradas na dica de ferramenta serão as propriedades de automação de interface do usuário no nível de elemento de prioridade mais alta. Se o **modo de elemento** for **Narrator** , as informações incluirão o texto que o Narrator lerá para o elemento.
- Selecione **Mostrar números** para exibir números de sequência que indicam a ordem de renderização de controle no layout. O esquema de número se baseia na configuração de **modo de elemento** :
    - **Controle folha**: os números indicam a ordem na qual os controles folha aparecem na árvore de automação da interface do usuário.
    - **Padrão de texto**: os números indicam a ordem em que os intervalos de texto aparecem em um intervalo de documentos.
    - **Narrador**: o número indica a ordem na qual os elementos são navegados na navegação do item do narrador.

## <a name="choosing-a-window"></a>Escolhendo uma janela

Na **janela** rótulo, você encontrará uma lista suspensa que lista todas as janelas de HWND que estão atualmente ativas no sistema. O texto de cada janela que aparece na lista suspensa é o título da janela e também uma ID de janela hexadecimal entre colchetes. Escolha um deles para alterar a janela de destino que o **AccScope** está relatando. Você pode escolher o mesmo item novamente para obter o mesmo comportamento que uma **atualização** explícita.

## <a name="using-the-accscope-visualization"></a>Usando a visualização AccScope

A imagem abaixo é uma captura de tela da visualização **AccScope** . Esta captura de tela específica mostra a ferramenta **AccScope** que exibe a janela de nível superior para a saída de [exemplo de acessibilidade XAML](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) , executando como um aplicativo no mesmo computador. Esta captura de tela mostra o modo de elemento padrão do **controle folha** e o valor **Visual** para **layout**.

![Captura de tela da visualização AccScope](images/accscopescreenshot.png)

Observe como essa visualização representa os controles no espaço aproximado de coordenadas que você veria no aplicativo. Mas, em vez de mostrar os visuais XAML ou o texto completo dos controles de texto, ele mostra os valores de propriedade de **nome** que vêm de cada elemento de controle, usando a automação da interface do usuário.

Além das opções de menu descritas anteriormente, você também pode usar estas técnicas:

- Clique no retângulo de qualquer elemento em **Visual** ou **listar** visualizações para exibir um pop-up de **Propriedades UIA** . Isso lista várias propriedades de automação de interface do usuário importantes para esse elemento, incluindo algumas das propriedades padrão do [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) e outras informações, como valores do Aria e uma **Descrição do provedor**.
- Clique com o botão direito do mouse no retângulo de qualquer elemento nas visualizações **Visual** ou **lista** para exibir um menu de contexto para exercer os padrões aos quais o elemento dá suporte. Por exemplo, se um elemento oferecer suporte a [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), o menu de contexto incluirá um item para **Invoke**. Selecione esse item e a API de padrão apropriada é exercitada no aplicativo correspondente. O **AccScope** dá suporte a esse recurso para os seguintes padrões: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Ajuste o controle deslizante **transparência** para alterar a opacidade/transparência da janela **AccScope** . Por padrão, ele é mostrado como 100% de opacidade. Tornar a janela transparente pode ser útil para ver as partes da janela de destino por meio da interface do usuário do **amAccScope** enquanto usa o modo de **Always on superior** .
- Se eles forem mostrados, use as barras de rolagem horizontal e vertical para alterar o centro de exibição da visualização. Isso será útil se você estiver usando a opção de layout **Visual** , mas não usar a opção de exibição de **tela inteira** , deixando a janela **AccScope** pequena em comparação com a janela de destino.

## <a name="testing-the-narrator-scenario"></a>Testando o cenário do narrador

O cenário do narrador é o aspecto mais importante a ser testado ao usar o **AccScope**, que foi projetado especificamente para visualizar como a navegação do item do narrador é feita quando é aplicada ao seu aplicativo.

Para testar o cenário do narrador, use estas opções de configuração do **AccScope** :

- **Modo de elemento**: **narrador**
- **Layout**: **Visual**
- Opções de **layout** : **Mostrar dica de ferramenta** e **Mostrar números** selecionados

Aqui estão algumas áreas específicas do seu aplicativo para testar o cenário do narrador:

- **Ordem do elemento:** Verifique se a ordem na qual o narrador lê os controles é precisa, de acordo com os números (círculos verdes) exibidos nas visualizações. Se os elementos não estiverem na ordem esperada para leitura, modifique a estrutura da interface do usuário do aplicativo e a árvore de automação da interface do usuário resultante e teste novamente até verificar se os elementos estão na ordem de leitura esperada.
- **Texto falado:** Mova o mouse na visualização e focalize cada um dos retângulos de elemento para exibir as dicas de ferramenta para cada elemento. No modo do narrador, as dicas de ferramenta exibem uma entrada de **texto do narrador** que é literalmente o texto que o Narrator lê. Geralmente, esse texto é composto do **nome** e do **tipo de controle**. Verifique se essas são as informações corretas para cada controle em sua interface do usuário. Se alguma informação estiver incorreta, modifique as propriedades de automação da interface do usuário por meio das técnicas habilitadas por sua estrutura de interface do usuário específica para fazer isso. (Se o **tipo de controle** for inesperado, talvez seja necessário usar um controle diferente, pois isso geralmente é controlado exclusivamente por implementações de controle da estrutura da interface do usuário.) Em seguida, teste novamente e verifique se **o texto do narrador** está correto.
- **Layout do elemento:** Verifique cada um desses casos:
    - Verifique se os elementos redundantes não são expostos pelo Narrator. Um exemplo de um elemento redundante é o controle de classificações em cada item de bloco da Windows Store.
    - Verifique se os elementos importantes (elementos que o usuário precisa para realizar as principais tarefas no aplicativo) são exibidos na navegação de itens do Narrator.
    - Se você estiver usando o layout **Visual** e um elemento estiver ausente porque os controles se sobrepõem, alterne para o layout da **lista** para ver a sequência que o narrador relata.
    - Verifique se a estrutura da árvore de automação da interface do usuário é precisa e esperada para seu aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Ferramentas de teste](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Verificação da Automação da Interface do Usuário](ui-automation-verify.md)
- [Acessibilidade da Microsoft](https://www.microsoft.com/accessibility/)
