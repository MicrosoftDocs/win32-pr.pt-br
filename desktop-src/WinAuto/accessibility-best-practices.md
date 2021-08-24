---
title: Práticas recomendadas de Acessibilidade
description: Implementar as melhores práticas descritas nesta seção ajuda a garantir que seu aplicativo seja acessível a pessoas que usam produtos de tecnologia adaptativa.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f596378c55b5f99af5b24fa60a23d980407392298fe2ad656579730fbab709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327866"
---
# <a name="accessibility-best-practices"></a>Práticas recomendadas de Acessibilidade

Implementar as melhores práticas descritas nesta seção ajuda a garantir que seu aplicativo seja acessível a pessoas que usam produtos de tecnologia adaptativa. Muitas dessas práticas recomendadas se concentram no bom design da interface do usuário. Cada melhor prática inclui informações de implementação para controles ou aplicativos. Em muitos casos, grande parte do trabalho para atender a essas práticas recomendadas já está incluída nos controles.

Este tópico inclui as seções a seguir.

-   [Acesso programático](#programmatic-access)
    -   [Habilitar o acesso programático a todos os elementos e textos da interface do usuário](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Colocar nomes, títulos e descrições em objetos, quadros e páginas da interface do usuário](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Garantir que eventos programáticos sejam disparados por todas as atividades da interface do usuário](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Usuário Configurações](#user-settings)
    -   [Respeitar todos os System-Wide Configurações e não interferir nas funções de acessibilidade](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Design da interface do usuário visual](#visual-ui-design)
    -   [Não Hard-Code cores](#do-not-hard-code-colors)
    -   [Suporte Alto Contraste e todos os atributos de exibição do sistema](#support-high-contrast-and-all-system-display-attributes)
    -   [Verifique se todas as interfaces do usuário são dimensionadas corretamente por qualquer configuração de DPI](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Navegação por teclado](#keyboard-navigation)
    -   [Fornecer interface do teclado para todos os elementos da interface do usuário](#provide-keyboard-interface-for-all-ui-elements)
    -   [Mostrar o foco do teclado](#show-the-keyboard-focus)
    -   [Suporte a padrões de navegação e esquemas de navegação poderosos](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Não permitir que a localização do mouse interfira na navegação do teclado](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Interface multi modal](#multi-modal-interface)
    -   [Fornecer User-Selectable equivalentes para elementos que não são de texto](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Usar cor, mas também fornecer alternativas à cor](#use-color-but-also-provide-alternatives-to-color)
    -   [Usar APIs de entrada padrão com chamadas Device-Independent padrão](#use-standard-input-apis-with-device-independent-calls)
-   [Tópicos relacionados](#related-topics)

## <a name="programmatic-access"></a>Acesso Programático

As práticas recomendadas nesta seção garantem que os produtos de tecnologia adaptativa tenham acesso programático adequado às informações e funcionalidades da interface do usuário.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Habilitar o acesso programático a todos os elementos e textos da interface do usuário

Os elementos de interface do usuário do seu aplicativo devem ser acessíveis programaticamente a produtos de tecnologia adaptativa. Todos os elementos da interface do usuário devem ter rótulos, devem expor todos os valores de propriedade e devem auar todos os eventos apropriados. Para os controles Windows padrão, a maior parte desse trabalho já é feita por meio do microsoft Automação da Interface do Usuário e Microsoft Active Accessibility de proxy. No entanto, os controles personalizados exigem trabalho adicional para garantir que eles sejam totalmente expostos para que os fornecedores de tecnologia adaptativa possam identificar e manipular elementos da interface do usuário do aplicativo.

Seguir essa melhor prática permite que os fornecedores de tecnologia adaptativa identifiquem e manipulem elementos da interface do usuário do seu produto.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Colocar nomes, títulos e descrições em objetos, quadros e páginas da interface do usuário

Como os produtos de tecnologia adaptativa, especialmente leitores de tela, usam títulos para entender a localização de um quadro, objeto ou página no esquema de navegação, os títulos devem ser muito descritivos. Bons títulos descritivos permitem que os produtos de tecnologia adaptativa identifiquem e manipulem elementos da interface do usuário em controles e aplicativos. Por exemplo, um título de página da Web de "Página da Web da Microsoft" será inútil se o usuário tiver navegado profundamente para uma área específica. Um título descritivo é crucial para usuários que são cegos e dependem de leitores de tela.

Seguir essa melhor prática permite que os produtos de tecnologia adaptativa identifiquem e manipulem a interface do usuário em aplicativos e controles de exemplo.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Garantir que eventos programáticos sejam disparados por todas as atividades da interface do usuário

Seu aplicativo deve agarr eventos sempre que ocorrerem alterações no estado ou na aparência de um elemento de interface do usuário.

Seguir essa melhor prática permite que os produtos de tecnologia adaptativa escutem as alterações na interface do usuário e notifiquem o usuário sobre essas alterações.

## <a name="user-settings"></a>Configurações do usuário

A melhor prática nesta seção garante que os controles ou aplicativos não substituam as configurações do usuário.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respeitar todos System-Wide Configurações e não interferir nas funções de acessibilidade

Os usuários podem usar Painel de Controle para definir alguns sinalizadores em todo o sistema; outros sinalizadores podem ser definidos programaticamente. Essas configurações não devem ser alteradas por controles ou aplicativos. Além disso, os aplicativos devem dar suporte às configurações de acessibilidade de seu sistema operacional host.

Seguir essa melhor prática permite aos usuários definir configurações de acessibilidade e saber que essas configurações não serão alteradas pelos aplicativos.

## <a name="visual-ui-design"></a>Design da interface do usuário visual

As práticas recomendadas nesta seção garantem que controles ou aplicativos usem cores e imagens com eficiência e possam ser usados por produtos de tecnologia adaptativa.

### <a name="do-not-hard-code-colors"></a>Não Hard-Code cores

Pessoas que não têm visão visual baixa ou estão usando uma tela preta e branca podem não ser capazes de usar aplicativos com cores em código.

Seguir essa melhor prática permite que os usuários ajustem combinações de cores com base em necessidades individuais.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Suporte Alto Contraste e todos os atributos de exibição do sistema

Os aplicativos não devem interromper nem desabilitar configurações de contraste, seleções de cores ou outros atributos e configurações de exibição de todo o sistema selecionados pelo usuário. As configurações de todo o sistema adotadas por um usuário aprimoram a acessibilidade dos aplicativos, portanto, eles não devem ser desabilitados nem desconsiderados pelos aplicativos. A cor deve ser usada em sua combinação correta de primeiro plano em segundo plano para fornecer contraste adequado. As cores não relacionadas não devem ser misturadas e as cores não devem ser invertidas.

Muitos usuários exigem combinações específicas de alto contraste, como texto em branco em uma fundo preta. Desenhando-os invertidos, pois o texto preto em um plano de fundo branco faz com que o plano de fundo se esvaia sobre o primeiro plano e pode dificultar a leitura para alguns usuários.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Verifique se todas as interfaces do usuário são dimensionadas corretamente por qualquer configuração de DPI

Verifique se todos os elementos da interface do usuário podem ser dimensionados corretamente por qualquer configuração de pontos por polegada (dpi). Além disso, verifique se os elementos da interface do usuário se encaixam em uma tela de 1024 x 768 com 120 pontos por polegada (dpi).

## <a name="keyboard-navigation"></a>Navegação por teclado

As práticas recomendadas nesta seção garantem que todas as funcionalidades do aplicativo estão acessíveis aos usuários que dependem do teclado.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Fornecer interface do teclado para todos os elementos da interface do usuário

As paradas de tabulação, especialmente quando cuidadosamente planejadas, dão aos usuários outra maneira de navegar pela interface do usuário.

Os aplicativos devem fornecer as seguintes interfaces de teclado:

-   Paradas de tabulação para todos os controles com os que o usuário pode interagir, como botões, links ou caixas de listagem.
-   Ordem de tabulação lógica.

### <a name="show-the-keyboard-focus"></a>Mostrar o foco do teclado

Os usuários precisam saber qual objeto tem o foco do teclado para que possam prever o efeito de seus toques de tecla. Para realçar o foco do teclado, use cores, fontes ou elementos gráficos, como retângulos ou ampliação. Para realçar de forma audível o foco do teclado, altere o volume, o tom ou a qualidade tonal.

Para evitar confusão, os aplicativos devem ocultar todos os indicadores de foco visual e seleções esmaecidas localizadas em janelas inativas (ou painéis).

Os aplicativos devem fazer o seguinte com o foco no teclado:

-   Um item sempre deve ter o foco do teclado.
-   O foco do teclado deve ser visível e óbvio.
-   As seleções e/ou itens focalizados devem ser realçadas visualmente.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Suporte a padrões de navegação e esquemas de navegação poderosos

Diferentes aspectos da navegação por teclado fornecem diferentes maneiras para os usuários navegarem pela interface do usuário.

Os aplicativos devem fornecer as seguintes interfaces de teclado:

-   Teclas de atalho e chaves de acesso sublinhadas para todos os comandos, menus e controles.
-   Atalhos de teclado para links importantes.
-   Todos os itens de menu têm uma chave de acesso; todos os botões têm teclas de acelerador, todos os comandos têm uma tecla de acelerador.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Não permitir que a localização do mouse interfira na navegação do teclado

O local do mouse não deve interferir na navegação do teclado. Por exemplo, se o mouse estiver posicionado e o usuário estiver navegando com o teclado, um clique do mouse não deverá acontecer, a menos que iniciado pelo usuário.

## <a name="multi-modal-interface"></a>Interface multi modal

A melhor prática nesta seção garante que a interface do usuário do aplicativo inclua alternativas para elementos visuais.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Fornecer User-Selectable equivalentes para elementos que não são de texto

Para cada elemento que não é de texto, forneça um equivalente selecionável pelo usuário para texto, transcrições ou descrições de áudio, como texto alt, legendas ou comentários visuais.

Elementos sem texto abrangem uma ampla variedade de elementos da interface do usuário, incluindo: imagens, regiões de mapa de imagem, animações, applets, quadros, scripts, botões gráficos, sons, arquivos de áudio e vídeo autônomos. Elementos que não são de texto são importantes quando contêm informações visuais, de fala ou de áudio geral às quais o usuário precisa acessar para entender o conteúdo da interface do usuário.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Usar cor, mas também fornecer alternativas à cor

Use a cor para aprimorar, enfatizar ou reter informações mostradas por outros meios, mas não comunicar informações usando apenas cores. Os usuários que não têm cor ou têm uma exibição monocromática precisam de alternativas para cores.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Usar APIs de Entrada Padrão com Device-Independent Chamadas

As chamadas independentes de dispositivo garantem que todos os dispositivos de entrada sejam tratados igualmente, fornecendo aos produtos de tecnologia adaptativa as informações necessárias sobre a interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Visão geral da API de Automação](windows-automation-api-overview.md)
</dt> </dl>

 

 




