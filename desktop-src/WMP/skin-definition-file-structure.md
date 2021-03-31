---
title: Estrutura do arquivo de definição de capa
description: Estrutura do arquivo de definição de capa
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, estrutura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005785"
---
# <a name="skin-definition-file-structure"></a>Estrutura do arquivo de definição de capa

O arquivo de definição de capa deve seguir uma estrutura específica. Você começa com um elemento **Theme** , cria um ou mais elementos **View** e, em seguida, define cada elemento **View** com os elementos da interface do usuário apropriados para o tipo de exibição que você deseja usar.

## <a name="theme-elements"></a>Elementos de tema

No nível superior, você deve iniciar o arquivo de definição de capa com o elemento **Theme** e fechá-lo.


```C++
<THEME>
    ...
</THEME>

```



O elemento **Theme** é o elemento raiz da sua capa. Pode haver apenas um elemento **Theme** em um arquivo de definição de capa e deve estar no nível superior. Os elementos de **tema** têm atributos específicos e de ambiente, embora a maioria das vezes não seja necessário usá-los. Para obter mais informações sobre esses atributos, consulte a [referência de programação de capa](skin-programming-reference.md).

## <a name="view-elements"></a>EXIBIR elementos

Cada **tema** deve ter pelo menos um elemento de **exibição** . O elemento **View** governa a imagem específica que você vê na tela. Talvez você queira ter mais de uma exibição, para que você possa alternar para frente e para trás. Por exemplo, talvez você queira ter uma exibição grande para trabalhar com listas de reprodução, uma exibição média para assistir a visualizações e uma pequena exibição que se encaixa em um canto da tela.

Se você estiver criando várias exibições, convém garantir que cada exibição tenha um valor de atributo de **ID** exclusivo que será usado para identificar a exibição. Você deve definir o atributo **backgroundImage** ou sua exibição não terá nenhuma imagem inicial. Se você não quiser exibir uma imagem retangular, provavelmente desejará usar o atributo **clippingColor** para definir as áreas da sua capa que não serão exibidas e provavelmente desejará definir o atributo **TitleBar** do elemento **View** .

Cada elemento **View** também pode ter um ou mais elementos **subview** . Um elemento de **subexibição** é semelhante a uma **exibição** e pode ser usado para partes da sua capa que você deseja mover, ocultar ou mostrar. Por exemplo, um elemento de **subexibição** pode ser usado para criar uma bandeja deslizante que se desprenda da sua capa para exibir um equalizador gráfico. Os elementos de **subexibição** podem ser alinhados com a **exibição** e ter outras relações especiais com a **exibição**.

## <a name="initializing-windows-media-player"></a>Inicializando o Windows Media Player

Você pode definir determinadas propriedades iniciais do Windows Media Player usando os elementos **Player**, **configurações** e **controles** . Por exemplo, você pode definir o volume para um nível inicial ou dar um valor padrão para um nome de arquivo.

O código a seguir mostra como definir o valor da **URL** em uma capa:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Se você quisesse definir o atributo **AutoStart** de **configurações** como false, usaria o seguinte código:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Observe que o elemento **Settings** está aninhado dentro do elemento **Player** .

Usando esses elementos, os seguintes atributos e eventos podem ser especificados em tempo de design:

**Atributos do elemento PLAYER**

-   **url**
-   **de resposta**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **Erro**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtatuschange**

**Atributos do elemento SETTINGS**

-   **Inicialização automática**
-   **Lance**
-   **baseURL**
-   **DefaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **Muta**
-   **playCount**
-   **frequência**
-   **volume**

## <a name="controls-element-attributes"></a>Atributos do elemento CONTROLS

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Outros elementos da interface do usuário

Depois de definir seus elementos **Theme** e **View** , você deve preencher sua **exibição** com elementos específicos da interface do usuário. Você não precisa usar todos os elementos disponíveis em uma capa, apenas aqueles que você precisa.

Se um elemento puder ser visto pelo usuário, ele será chamado de controle. Os seguintes controles estão disponíveis para capas:

-   Botões
-   Controles deslizantes, controles deslizantes personalizados e barras de progresso
-   Caixas de texto
-   Janelas de vídeo
-   Janelas de visualização
-   Janelas de lista de reprodução
-   Janelas de subexibição

Além disso, vários elementos podem ser usados para definir ainda mais as ações do Windows Media Player, mas exigem elementos visuais, como botões ou controles deslizantes:

-   Configurações de vídeo
-   Configurações do equalizador
-   Configurações de visualização

## <a name="buttons"></a>Botões

Os botões são a parte mais popular de uma capa. Você pode usar botões para disparar ações como reproduzir, parar, encerrar, minimizar e alternar para modo de exibição diferente. O Windows Media Player fornece o criador da capa com dois tipos de elementos Button: o elemento **Button** e o elemento **Button** . Além disso, há vários tipos predefinidos de botões.

-   **Elemento BUTTON.** O elemento **Button** é usado para botões individuais. Se você usar o elemento **Button** , deverá fornecer uma imagem para cada botão e definir o local exato onde você deseja que o botão apareça em relação à imagem de plano de fundo. Uma das vantagens do elemento **Button** é que você pode alterar a imagem do botão dinamicamente.
-   **Elemento de botão.** O elemento do grupo **de botões é** usado para grupos de botões. Na verdade, você deve colocar cada elemento de um dos **botões** com um par de marcas de **botão** . O uso de grupos de botões é mais fácil do que usar botões individuais, pois você não precisa especificar o local exato para cada botão. Em vez disso, você fornece um mapa de imagem separado que define as ações que ocorrerão quando o mouse passar sobre ou clicar em uma área em seu plano de fundo. Usar mapas de imagem é fácil porque você pode pegar a arte criada para seu plano de fundo e copiá-la para uma camada de mapeamento em seu programa de edição de elementos gráficos. Usar o programa de edição de elementos gráficos é mais rápido e preciso do que tentar definir exatamente onde um botão individual deve ser colocado em seu plano de fundo.
-   **Botões predefinidos.** Há vários botões predefinidos. Por exemplo, você pode usar um botão PLAYelement para reproduzir arquivos de mídia digital e um STOPelement para parar a reprodução. Consulte [elemento de botão](buttongroup-element.md) e [elemento Button](button-element.md) na referência de programação de capa. O [IMAGEBUTTON](imagebutton.md) pode ser usado para exibir imagens que podem ser alteradas em resposta a eventos específicos.

## <a name="sliders"></a>Controles deslizantes

Os controles deslizantes são úteis para trabalhar com informações que mudam ao longo do tempo. Por exemplo, você pode usar um controle deslizante para indicar a quantidade de músicas que já foram reproduzidas para um arquivo de mídia específico. Os controles deslizantes podem ser horizontais, verticais, lineares ou circulares ou qualquer forma que você possa imaginar. Os controles deslizantes são fornecidos em três variedades: controles deslizantes, barras de progresso e controles deslizantes personalizados.

-   **Controles deslizantes.** Você pode usar o elemento **Slider** para controles de volume ou para permitir que o usuário se mova para uma parte diferente do conteúdo de mídia.
-   **Barras de progresso.** As barras de progresso são semelhantes aos controles deslizantes. As barras de progresso são projetadas para exibir graficamente a porcentagem de um processo específico que foi concluído, mas não para um processo com o qual o usuário desejará interagir. Por exemplo, talvez você queira usar uma barra de progresso para indicar o progresso do buffer.
-   **Controles deslizantes personalizados.** A funcionalidade de controle deslizante personalizado é fornecida para que você possa criar controles como botões ou criar mecanismos de controle incomuns. Por exemplo, se você quiser criar um controle de volume que encapsula em sua capa, poderá fazê-lo com um controle deslizante personalizado. Para configurar o controle deslizante personalizado, você deve criar um mapa de imagem que contenha imagens em escala de cinza para definir os locais dos valores no controle deslizante. Isso é relativamente fácil de fazer com um programa de edição de gráficos que dá suporte a camadas.

## <a name="text"></a>Texto

Você pode usar o elemento de **texto** para exibir o texto em sua capa, como títulos de música.

## <a name="video"></a>Vídeo

Você pode exibir o vídeo em sua capa. O elemento **Video** permite que você defina o tamanho e a posição da janela de vídeo.

Você também pode permitir que o usuário altere as configurações de vídeo com o elemento **VIDEOSETTINGS** . Por exemplo, você pode criar controles para ajustar o brilho do vídeo.

Se você não fornecer um elemento de vídeo e o conteúdo contiver vídeo, o Windows Media Player retornará ao modo completo e sua capa não será exibida.

## <a name="equalizer-settings"></a>Configurações do equalizador

Você pode definir a filtragem para faixas de frequência de áudio específicas usando o elemento **EQUALIZERSETTINGS** . Você pode aumentar os graves, ajustar os agudos e configurar seus sons para que correspondam aos ouvidos ou à sala de vida.

## <a name="visualizations"></a>Visualizações

Você pode exibir visualizações em sua capa. As visualizações são efeitos visuais que mudam com o passar do tempo conforme o áudio é executado pelo Windows Media Player. O elemento **Effects** determina onde as visualizações serão reproduzidas, qual será o tamanho da janela e quais visualizações serão reproduzidas.

## <a name="playlists"></a>Playlists

Você pode usar o elemento **playlist** para permitir que o usuário selecione um item de uma lista de reprodução específica.

## <a name="subviews"></a>Subexibições

Você pode usar o elemento **subview** para exibir conjuntos secundários de controles de interface, como uma playlist ou controles de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de capa**](skin-files.md)
</dt> </dl>

 

 




