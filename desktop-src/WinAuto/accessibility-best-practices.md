---
title: Práticas recomendadas de Acessibilidade
description: A implementação das práticas recomendadas descritas nesta seção ajuda a garantir que seu aplicativo possa ser acessado por pessoas que usam produtos de tecnologia assistencial.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d9f70828610d04255b61ad3ee533d23c514867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822523"
---
# <a name="accessibility-best-practices"></a>Práticas recomendadas de Acessibilidade

A implementação das práticas recomendadas descritas nesta seção ajuda a garantir que seu aplicativo possa ser acessado por pessoas que usam produtos de tecnologia assistencial. Muitas dessas práticas recomendadas se concentram em um bom design de interface do usuário. Cada prática recomendada inclui informações de implementação para controles ou aplicativos. Em muitos casos, grande parte do trabalho para atender a essas práticas recomendadas já está incluída nos controles.

Este tópico inclui as seções a seguir.

-   [Acesso programático](#programmatic-access)
    -   [Habilitar o acesso programático a todos os elementos e texto da interface do usuário](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Coloque nomes, títulos e descrições em objetos, quadros e páginas da interface do usuário](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Garantir que eventos programáticos sejam disparados por todas as atividades de IU](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Configurações do usuário](#user-settings)
    -   [Respeitar todas as configurações de System-Wide e não interferem nas funções de acessibilidade](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Design de interface do usuário Visual](#visual-ui-design)
    -   [Não Hard-Code cores](#do-not-hard-code-colors)
    -   [Suporte a Alto Contraste e todos os atributos de exibição do sistema](#support-high-contrast-and-all-system-display-attributes)
    -   [Garantir que toda a interface do usuário seja dimensionada corretamente por qualquer configuração de DPI](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Navegação por teclado](#keyboard-navigation)
    -   [Fornecer interface de teclado para todos os elementos da interface do usuário](#provide-keyboard-interface-for-all-ui-elements)
    -   [Mostrar o foco do teclado](#show-the-keyboard-focus)
    -   [Suporte a padrões de navegação e esquemas de navegação avançados](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Não permitir que o local do mouse interfira na navegação do teclado](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Interface multimodal](#multi-modal-interface)
    -   [Fornecer User-Selectable equivalentes para elementos que não são de texto](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Usar cor, mas também fornecer alternativas para cor](#use-color-but-also-provide-alternatives-to-color)
    -   [Usar APIs de entrada padrão com chamadas de Device-Independent](#use-standard-input-apis-with-device-independent-calls)
-   [Tópicos relacionados](#related-topics)

## <a name="programmatic-access"></a>Acesso Programático

As práticas recomendadas nesta seção enurem que produtos de tecnologia assistencial têm acesso programático adequado a informações e funcionalidades da interface do usuário.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Habilitar o acesso programático a todos os elementos e texto da interface do usuário

Os elementos da interface do usuário do seu aplicativo devem ser acessados programaticamente para produtos de tecnologia assistencial. Todos os elementos da interface do usuário devem ter rótulos, devem expor todos os valores de propriedade e devem gerar todos os eventos apropriados. Para os controles padrão do Windows, a maior parte desse trabalho já foi feita por meio da automação da interface do usuário da Microsoft e dos objetos de proxy do Microsoft Acessibilidade Ativa. Os controles personalizados, no entanto, exigem trabalho adicional para garantir que eles sejam totalmente expostos para que os fornecedores de tecnologia assistencial possam identificar e manipular elementos de sua interface do usuário do aplicativo.

Seguir essa prática recomendada permite que fornecedores de tecnologia assistencial identifiquem e manipulem elementos da interface do usuário do produto.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Coloque nomes, títulos e descrições em objetos, quadros e páginas da interface do usuário

Como os produtos de tecnologia assistencial — especialmente leitores de tela — usam títulos para entender o local de um quadro, objeto ou página no esquema de navegação, os títulos devem ser muito descritivos. Bons títulos descritivos permitem que produtos de tecnologia assistencial identifiquem e manipulem elementos de interface do usuário em controles e aplicativos. Por exemplo, um título de página da Web de "página da Microsoft" é inútil se o usuário navegou profundamente em uma área específica. Um título descritivo é crucial para os usuários que são cegos e dependem de leitores de tela.

Seguir essa prática recomendada permite que produtos de tecnologia assistencial identifiquem e manipulem a interface do usuário em aplicativos e controles de exemplo.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Garantir que eventos programáticos sejam disparados por todas as atividades de IU

Seu aplicativo deve gerar eventos sempre que ocorrerem alterações no estado ou na aparência de um elemento de interface do usuário.

Seguir essa prática recomendada permite que os produtos de tecnologia assistencial escutem as alterações na interface do usuário e Notifiquem os usuários sobre essas alterações.

## <a name="user-settings"></a>Configurações do usuário

A prática recomendada nesta seção garante que os controles ou aplicativos não substituam as configurações do usuário.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respeitar todas as configurações de System-Wide e não interferem nas funções de acessibilidade

Os usuários podem usar o painel de controle para definir alguns sinalizadores de todo o sistema; outros sinalizadores podem ser definidos programaticamente. Essas configurações não devem ser alteradas por controles ou aplicativos. Além disso, os aplicativos devem dar suporte às configurações de acessibilidade do sistema operacional do host.

Seguir essa prática recomendada permite que os usuários definam as configurações de acessibilidade e saibam que essas configurações não serão alteradas pelos aplicativos.

## <a name="visual-ui-design"></a>Design de interface do usuário Visual

As práticas recomendadas nesta seção garantem que os controles ou aplicativos usem cores e imagens com eficiência e possam ser usados por produtos de tecnologia assistencial.

### <a name="do-not-hard-code-colors"></a>Não Hard-Code cores

As pessoas que têm cores cegas, têm pouca visão ou estão usando uma tela preta e branca podem não ser capazes de usar aplicativos com cores embutidas em código.

Seguir essa prática recomendada permite que os usuários ajustem combinações de cores com base em necessidades individuais.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Suporte a Alto Contraste e todos os atributos de exibição do sistema

Os aplicativos não devem interromper ou desabilitar as configurações de contraste de todo o sistema, selecionadas pelo usuário, seleções de cores ou outras configurações de vídeo e atributos de todo o sistema. As configurações de todo o sistema adotadas por um usuário aprimoram a acessibilidade dos aplicativos, portanto, eles não devem ser desabilitados ou desconsiderados por aplicativos. A cor deve ser usada em sua combinação correta de primeiro plano em segundo plano para fornecer um contraste adequado. As cores não relacionadas não devem ser misturadas e as cores não devem ser revertidas.

Muitos usuários exigem combinações específicas de alto contraste, como texto em branco em um plano de fundo preto. Desenhar esses invertidos, como texto preto em um plano de fundo branco, faz com que o plano de fundo seja sangrado em primeiro plano e pode dificultar a leitura para alguns usuários.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Garantir que toda a interface do usuário seja dimensionada corretamente por qualquer configuração de DPI

Verifique se todos os elementos da interface do usuário podem ser dimensionados corretamente por qualquer configuração de pontos por polegada (DPI). Além disso, verifique se os elementos da interface do usuário se encaixam em uma tela de 1024 x 768 com 120 pontos por polegada (DPI).

## <a name="keyboard-navigation"></a>Navegação por teclado

As práticas recomendadas nesta seção garantem que toda a funcionalidade do aplicativo seja acessível aos usuários que dependem do teclado.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Fornecer interface de teclado para todos os elementos da interface do usuário

As paradas de tabulação, especialmente quando planejadas cuidadosamente, dão aos usuários outra maneira de navegar pela interface do usuário.

Os aplicativos devem fornecer as seguintes interfaces de teclado:

-   Tabulações para todos os controles com os quais o usuário pode interagir, como botões, links ou caixas de listagem.
-   Ordem de tabulação lógica.

### <a name="show-the-keyboard-focus"></a>Mostrar o foco do teclado

Os usuários precisam saber qual objeto tem o foco do teclado para que eles possam prever o efeito de seus pressionamentos de teclas. Para destacar o foco do teclado, use cores, fontes ou elementos gráficos, como retângulos ou ampliação. Para forma audível realçar o foco do teclado, altere a qualidade do volume, da densidade ou do Tom.

Para evitar confusão, os aplicativos devem ocultar todos os indicadores de foco visual e as seleções Dim que estão localizadas em janelas inativas (ou painéis).

Os aplicativos devem fazer o seguinte com o foco do teclado:

-   Um item sempre deve ter o foco do teclado.
-   O foco do teclado deve ser visível e óbvio.
-   As seleções e/ou os itens focados devem ser visualmente realçados.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Suporte a padrões de navegação e esquemas de navegação avançados

Diferentes aspectos da navegação por teclado fornecem maneiras diferentes para os usuários navegarem pela interface do usuário.

Os aplicativos devem fornecer as seguintes interfaces de teclado:

-   Teclas de atalho e chaves de acesso sublinhadas para todos os comandos, menus e controles.
-   Atalhos de teclado para links importantes.
-   Todos os itens de menu têm uma chave de acesso; todos os botões têm teclas de aceleração, todos os comandos têm uma tecla aceleradora.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Não permitir que o local do mouse interfira na navegação do teclado

O local do mouse não deve interferir na navegação do teclado. Por exemplo, se o mouse estiver posicionado em algum lugar e o usuário estiver navegando com o teclado, um clique do mouse não deverá ocorrer a menos que seja iniciado pelo usuário.

## <a name="multi-modal-interface"></a>Interface multimodal

A prática recomendada nesta seção garante que a interface do usuário do aplicativo inclua alternativas para elementos visuais.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Fornecer User-Selectable equivalentes para elementos que não são de texto

Para cada elemento que não seja texto, forneça um equivalente selecionável pelo usuário para texto, transcrições ou descrições de áudio, como texto alternativo, legendas ou comentários visuais.

Elementos sem texto abrangem uma ampla gama de elementos da interface do usuário, incluindo: imagens, regiões de mapa de imagem, animações, applets, quadros, scripts, botões gráficos, sons, arquivos de áudio autônomos e vídeo. Elementos que não são de texto são importantes quando contêm informações visuais, fala ou informações gerais de áudio que o usuário precisa acessar para entender o conteúdo da interface do usuário.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Usar cor, mas também fornecer alternativas para cor

Use cores para aprimorar, enfatizar ou reiterar as informações mostradas por outros meios, mas não comunicar informações usando apenas a cor. Os usuários que têm cores cegas ou têm um monitor monocromático precisam de alternativas para cores.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Usar APIs de entrada padrão com chamadas de Device-Independent

As chamadas independentes de dispositivo garantem que todos os dispositivos de entrada sejam tratados igualmente, ao mesmo tempo em que fornecem produtos de tecnologia assistencial com as informações necessárias sobre a interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da API de automação do Windows](windows-automation-api-overview.md)
</dt> </dl>

 

 




