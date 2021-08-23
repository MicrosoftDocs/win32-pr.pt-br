---
title: Estrutura do arquivo de definição de capa
description: Estrutura do arquivo de definição de capa
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Windows Media Player capas, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, estrutura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c708e46f93e2d00820015a04b0f467da2deafe59e4dbafb0b9e4f3fb8660271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995266"
---
# <a name="skin-definition-file-structure"></a>Estrutura do arquivo de definição de capa

O arquivo de definição de capa deve seguir uma estrutura específica. Você começa com um **elemento THEME,** cria um ou mais elementos **VIEW** e define cada elemento **VIEW** com os elementos de interface do usuário apropriados para o tipo de exibição que você deseja usar.

## <a name="theme-elements"></a>Elementos THEME

No nível superior, você deve iniciar o arquivo de definição de capa com o **elemento THEME** e fechar com ele.


```C++
<THEME>
    ...
</THEME>

```



O **elemento THEME** é o elemento raiz da sua capa. Pode haver apenas um elemento **THEME** em um arquivo de definição de capa e ele deve estar no nível superior. **Os** elementos THEME têm atributos específicos e de ambiente, embora na maioria das vezes você não precise usá-los. Para obter mais informações sobre esses atributos, consulte a Referência [de programação de capa](skin-programming-reference.md).

## <a name="view-elements"></a>Elementos VIEW

Cada **THEME** deve ter pelo menos um **elemento VIEW.** O **elemento VIEW** rege a imagem específica que você vê na tela. Talvez você queira ter mais de uma exibição, para poder alternar para frente e para trás. Por exemplo, talvez você queira ter uma exibição grande para trabalhar com playlists, uma exibição média para assistir a visualizações e uma exibição pequena que caiba em um canto da tela.

Se você estiver criando várias exibições, certifique-se de que cada exibição tenha um valor de atributo **de ID** exclusivo que será usado para identificar a exibição. Você deve definir o **atributo backgroundImage** ou sua exibição não terá nenhuma imagem inicial. Se você não quiser exibir uma imagem retangular, provavelmente será melhor usar o atributo **clippingColor** para definir as áreas da sua capa que não serão exibidas e, provavelmente, você deseja definir o atributo **titleBar** do elemento **VIEW.**

Cada **elemento VIEW** também pode ter um ou mais elementos **SUBVIEW.** Um **elemento SUBVIEW** é semelhante a **um VIEW** e pode ser usado para partes da sua capa que você deseja mover, ocultar ou mostrar. Por exemplo, um **elemento SUBVIEW** pode ser usado para criar uma bandeja deslizante que sai da sua capa para exibir um equalizador gráfico. **Os elementos SUBVIEW** podem ser alinhados com **VIEW** e ter outras relações especiais com a **VIEW**.

## <a name="initializing-windows-media-player"></a>Inicializando Windows Media Player

Você pode definir determinadas propriedades iniciais Windows Media Player usando os **elementos PLAYER,** **SETTINGS** e **CONTROLS.** Por exemplo, você pode definir o volume para um nível inicial ou dar um valor padrão para um nome de arquivo.

O código a seguir mostra como definir o **valor da URL** em uma capa:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Se você quisesse definir o **atributo autoStart** de **SETTINGS** como False, usaria o seguinte código:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Observe que o **elemento SETTINGS** está aninhado dentro do **elemento PLAYER.**

Usando esses elementos, os seguintes atributos e eventos podem ser especificados em tempo de design:

**Atributos de elemento PLAYER**

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

**Atributos de elemento SETTINGS**

-   **Autostart**
-   **Equilíbrio**
-   **Baseurl**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **Invokeurls**
-   **Mudo**
-   **playCount**
-   **Taxa**
-   **volume**

## <a name="controls-element-attributes"></a>Atributos de elemento CONTROLS

-   **Currentmarker**
-   **Currentposition**

## <a name="other-user-interface-elements"></a>Outros Interface do Usuário elementos

Depois de definir os elementos **THEME** e **VIEW,** você deve preencher o **VIEW** com elementos específicos da interface do usuário. Você não precisa usar todos os elementos disponíveis em uma capa, apenas aqueles de que precisa.

Se um elemento puder ser visto pelo usuário, ele será chamado de controle. Os seguintes controles estão disponíveis para capas:

-   Botões
-   Controles deslizantes, controles deslizantes personalizados e barras de progresso
-   Caixas de texto
-   Janelas de vídeo
-   Janelas de visualização
-   Janelas de playlist
-   Janelas de subvisão

Além disso, vários elementos podem ser usados para definir ainda mais Windows Media Player ações, mas exigem elementos visuais, como botões ou controles deslizantes:

-   Configurações de vídeo
-   Equalizer Configurações
-   Configurações de visualização

## <a name="buttons"></a>Botões

Os botões são a parte mais popular de uma capa. Você pode usar botões para disparar ações como reproduzir, parar, encerrar, minimizar e alternar para uma exibição diferente. Windows Media Player fornece ao criador de capa dois tipos de elementos de botão: o **elemento BUTTON** e o **elemento BUTTONGROUP.** Além disso, há vários tipos predefinidos de botões.

-   **Elemento BUTTON.** O **elemento BUTTON** é usado para botões individuais. Se você usar o **elemento BUTTON,** deverá fornecer uma imagem para cada botão e definir o local exato em que deseja que o botão apareça em relação à imagem de plano de fundo. Uma das vantagens do elemento **BUTTON** é que você pode alterar a imagem do botão dinamicamente.
-   **Elemento BUTTONGROUP.** O **elemento BUTTONGROUP** é usado para grupos de botões. Na verdade, você deve incluir cada **elemento BUTTONGROUP** com um par de marcas **BUTTONGROUP.** Usar grupos de botões é mais fácil do que usar botões individuais porque você não precisa especificar o local exato para cada botão. Em vez disso, você fornece um mapa de imagem separado que define as ações que ocorrerão quando o mouse passar o mouse sobre ou clicar em uma área em sua plano de fundo. Usar mapas de imagem é fácil porque você pode pegar a arte criada para sua plano de fundo e copiá-la para uma camada de mapeamento em seu programa de edição de gráficos. O uso do programa de edição de gráficos é mais rápido e preciso do que tentar definir exatamente onde um botão individual deve ser colocado em sua plano de fundo.
-   **Botões predefinidos.** Há vários botões predefinidos. Por exemplo, você pode usar um botão PLAYELEMENT para reproduzir arquivos de mídia digital e um STOPELEMENT para interromper a reprodução. Consulte [Elemento BUTTONGROUP](buttongroup-element.md) e [Elemento BUTTON](button-element.md) na Referência de programação de capa. O [IMAGEBUTTON](imagebutton.md) pode ser usado para exibir imagens que podem ser alteradas em resposta a eventos específicos.

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

se você não fornecer um elemento de vídeo e o conteúdo contiver vídeo, Windows Media Player retornará ao modo completo e sua capa não será exibida.

## <a name="equalizer-settings"></a>Configurações do equalizador

Você pode definir a filtragem para faixas de frequência de áudio específicas usando o elemento **EQUALIZERSETTINGS** . Você pode aumentar os graves, ajustar os agudos e configurar seus sons para que correspondam aos ouvidos ou à sala de vida.

## <a name="visualizations"></a>Visualizações

Você pode exibir visualizações em sua capa. As visualizações são efeitos visuais que mudam ao longo do tempo conforme o áudio é executado por meio de Windows Media Player. O elemento **Effects** determina onde as visualizações serão reproduzidas, qual será o tamanho da janela e quais visualizações serão reproduzidas.

## <a name="playlists"></a>Playlists

Você pode usar o elemento **playlist** para permitir que o usuário selecione um item de uma lista de reprodução específica.

## <a name="subviews"></a>Subexibições

Você pode usar o elemento **subview** para exibir conjuntos secundários de controles de interface, como uma playlist ou controles de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de capa**](skin-files.md)
</dt> </dl>

 

 




