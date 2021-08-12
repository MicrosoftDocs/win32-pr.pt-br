---
title: Sobre listas de imagens
description: Uma lista de imagens é uma coleção de imagens do mesmo tamanho, cada uma das quais pode ser referenciada por seu índice.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfbb55ecd972e7f7e257eebabdb94ee40846a4f1b70b2a725ae1b67c6e69e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672197"
---
# <a name="about-image-lists"></a>Sobre listas de imagens

Uma lista de imagens é uma coleção de imagens do mesmo tamanho, cada uma das quais pode ser referenciada por seu índice. As listas de imagens são usadas para gerenciar com eficiência grandes conjuntos de ícones ou bitmaps. Todas as imagens em uma lista de imagens estão contidas em um único bitmap largo no formato de dispositivo de tela. Uma lista de imagens também pode incluir um bitmap monocromático que contém máscaras usadas para desenhar imagens de forma transparente (estilo de ícone).

A API do Microsoft Win32 fornece funções e macros de lista de imagens que permitem criar e destruir listas de imagens, adicionar e remover imagens, substituir e mesclar imagens, desenhar imagens e arrastar imagens. Para usar as funções de lista de imagens, inclua o arquivo de título de controle comum em seus arquivos de código-fonte e vincule-o à biblioteca de exportação de controle comum. Além disso, antes de chamar qualquer função de lista de imagens, use a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para garantir que a DLL de controle comum seja carregada.

Os seguintes tópicos são discutidos nesta seção:

-   [Types](#types)
-   [Criando e destrói listas de imagens](#creating-and-destroying-image-lists)
-   [Adicionando e removendo imagens](#adding-and-removing-images)
-   [Substituindo e mesclando imagens](#replacing-and-merging-images)
-   [Desenhando imagens](#drawing-images)
-   [Arrastando imagens](#dragging-images)
-   [Informações da imagem](#image-information)
-   [Sobreposições de imagem](#image-overlays)
-   [Ícones antialiados de 32 bits](#32-bit-antialiased-icons)

## <a name="types"></a>Tipos

Há dois tipos de listas de imagens: não mascarada e mascarada. Uma lista de imagens não máscaradas consiste em um bitmap de cor que contém uma ou mais imagens. Uma lista de imagens mascaradas consiste em dois bitmaps de tamanho igual. O primeiro é um bitmap de cor que contém as imagens e o segundo é um bitmap monocromático que contém uma série de máscaras – uma para cada imagem no primeiro bitmap.

Quando uma imagem não máscara é desenhada, ela é simplesmente copiada para o contexto do dispositivo de destino; ou seja, ele é desenhado sobre a cor da tela de fundo existente do contexto do dispositivo. Quando uma imagem mascarada é desenhada, os bits da imagem são combinados com os bits da máscara, normalmente produzindo áreas transparentes no bitmap em que a cor da tela de fundo do contexto do dispositivo de destino aparece. Há vários estilos de desenho que você pode especificar ao desenhar uma imagem mascarada. Por exemplo, você pode especificar que a imagem seja dithered para indicar um objeto selecionado.

## <a name="creating-and-destroying-image-lists"></a>Criando e destrói listas de imagens

Crie uma lista de imagens chamando a [**função ImageList \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) Os parâmetros incluem o tipo de lista de imagens a ser criado, as dimensões de cada imagem e o número de imagens que você pretende adicionar à lista. Para uma lista de imagens não máscaradas, a função cria um único bitmap grande o suficiente para manter o número especificado de imagens das dimensões determinadas. Em seguida, ele cria um contexto de dispositivo compatível com a tela e seleciona o bitmap nele. Para uma lista de imagens mascaradas, a função cria dois bitmaps e dois contextos de dispositivo compatíveis com a tela. Ele seleciona o bitmap de imagem em um contexto de dispositivo e o bitmap de máscara no outro. A DLL de controle comum contém o código executável para as funções de lista de imagens.

Em [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), especifique o número inicial de imagens que estarão em uma lista de imagens, bem como o número de imagens pelas quais a lista pode crescer. Portanto, se você tentar adicionar mais imagens do que especificou inicialmente, a lista de imagens aumentará automaticamente para acomodar as novas imagens.

Se [**ImageList \_ Create for**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) bem-sucedido, ele retornará um identificador para o tipo HIMAGELIST. Use esse handle em outras funções de lista de imagens para acessar a lista de imagens e gerenciar as imagens. Você pode adicionar e remover imagens, copiar imagens de uma lista de imagens para outra e mesclar imagens de duas listas de imagens diferentes. Quando você não precisar mais de uma lista de imagens, poderá destruir especificando seu alça em uma chamada para a [**função ImageList \_ Destroy.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)

## <a name="adding-and-removing-images"></a>Adicionando e removendo imagens

Você pode adicionar imagens bit a bit, ícones ou cursores a uma lista de imagens. Adicione imagens bit a bit especificando os alças a dois bitmaps em uma chamada para a [**função ImageList \_ Add.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) O primeiro bitmap contém uma ou mais imagens a adicionar ao bitmap de imagem e o segundo bitmap contém as máscaras a adicionar ao bitmap de máscara. Para listas de imagens não máscaradas, o segundo alça de bitmap é ignorado; ele pode ser definido como **NULL.**

A [**função \_ ImageList AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) também adiciona imagens bitmapped a uma lista de imagens mascaradas. Essa função é semelhante a [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), exceto que você não especifica um bitmap de máscara. Em vez disso, você especifica uma cor que o sistema combina com o bitmap de imagem para gerar automaticamente as máscaras. Cada pixel da cor especificada no bitmap da imagem é alterado para preto e o bit correspondente na máscara é definido como 1. Como resultado, qualquer pixel na imagem que corresponde à cor especificada é transparente quando a imagem é desenhada.

A [**macro \_ ImageList AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) adiciona um ícone ou cursor a uma lista de imagens. Se a lista de imagens estiver mascarada, **ImageList \_ AddIcon** adicionará a máscara fornecida com o ícone ou cursor ao bitmap de máscara. Se a lista de imagens não for mascarada, a máscara para o ícone ou cursor não será usada ao desenhar a imagem.

Você pode criar um ícone com base em uma imagem e mascarar em uma lista de imagens usando a [**função \_ ImageList GetIcon.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) A função retorna o alça para o novo ícone.

[**ImageList \_ Adicione**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)e [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) atribuam um índice a cada imagem à medida que ele é adicionado a uma lista de imagens. Os índices são baseados em zero; ou seja, a primeira imagem na lista tem um índice de zero, a próxima tem um índice de um e assim por diante. Depois de adicionar uma única imagem, as funções retornam o índice da imagem. Quando mais de uma imagem é adicionada por vez, as funções retornam o índice da primeira imagem.

A [**função ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) remove uma imagem de uma lista de imagens.

## <a name="replacing-and-merging-images"></a>Substituindo e mesclando imagens

As [**funções ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) e [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) substituem uma imagem em uma lista de imagens por uma nova imagem. **ImageList \_ Substituir** substitui uma imagem por uma imagem mapeada e uma máscara, e **ImageList \_ ReplaceIcon** substitui uma imagem por um ícone ou cursor.

A [**função ImageList \_ Merge**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) mescla duas imagens, armazenar a nova imagem em uma nova lista de imagens. A nova imagem é criada desenhando a segunda imagem de forma transparente sobre a primeira. A máscara para a nova imagem é o resultado da execução de uma operação **OR lógica** nos bits das máscaras para as duas imagens existentes.

## <a name="drawing-images"></a>Desenhando imagens

Para desenhar uma imagem, use a função [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Especifique o handle para uma lista de imagens, o índice da imagem a ser desenhada, o handle para o contexto do dispositivo de destino, um local dentro do contexto do dispositivo e um ou mais estilos de desenho.

Quando você especifica o estilo **TRANSPARENTE \_ ILD,** [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) usa um processo de duas etapas para desenhar uma imagem mascarada. Primeiro, ele executa uma operação **AND lógica** nos bits da imagem e nos bits da máscara. Em seguida, ele executa uma operação **XOR lógica** nos resultados da primeira operação e nos bits em segundo plano do contexto do dispositivo de destino. Esse processo cria áreas transparentes na imagem resultante; ou seja, cada bit em branco na máscara faz com que o bit correspondente na imagem resultante seja transparente.

Antes de desenhar uma imagem mascarada em uma tela de fundo de cor sólida, você deve usar a função [**\_ ImageList SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) para definir a cor da tela de fundo da lista de imagens com a mesma cor que o destino. Definir a cor elimina a necessidade de criar áreas transparentes na imagem e permite que [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) simplesmente copie a imagem para o contexto do dispositivo de destino, resultando em um aumento significativo no desempenho. Para desenhar a imagem, especifique o **estilo ILD \_ NORMAL** em uma chamada para **ImageList \_ Draw** ou **ImageList \_ DrawEx.**

Você pode definir a cor da tela de fundo para uma lista de imagens mascaradas a qualquer momento para que ela seja desenhada corretamente em qualquer tela de fundo sólida. Definir a cor da tela de fundo como CLR \_ NONE faz com que as imagens sejam desenhadas de forma transparente por padrão. Para recuperar a cor da tela de fundo de uma lista de imagens, use a [**função \_ ImageList GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)

Os **estilos ILD \_ BLEND25** e **ILD \_ BLEND50** mesclam a imagem com a cor de realçada do sistema. Esses estilos serão úteis se você usar uma imagem mascarada para representar um objeto que o usuário pode selecionar. Por exemplo, você pode usar o estilo **ILD \_ BLEND50** para desenhar a imagem quando o usuário a seleciona.

Uma imagem não máscarada é copiada para o contexto do dispositivo de destino usando a operação de varredura SRCCOPY. As cores na imagem aparecem da mesma forma, independentemente da cor da tela de fundo do contexto do dispositivo. Os estilos de desenho especificados em [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) também não têm nenhum efeito na aparência de uma imagem não máscarada.

## <a name="dragging-images"></a>Arrastando imagens

A API do Win32 inclui funções para arrastar uma imagem na tela. As funções de arrastar movem uma imagem sem problemas, em cores e sem nenhuma piscação do cursor. Imagens mascaradas e não mascaradas podem ser arrastadas.

A [**função \_ ImageList BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) inicia uma operação de arrastar. Os parâmetros incluem o alça para a lista de imagens, o índice da imagem a ser arrastada e o local do ponto de calor dentro da imagem. O ponto de calor é um único pixel que as funções de arrastar reconhecem como o local exato da tela da imagem. Normalmente, um aplicativo define o ponto de contato para que ele coincida com o ponto quente do cursor do mouse. A [**função ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) move a imagem para um novo local.

A [**função \_ ImageList DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) define a posição inicial da imagem de arrastar dentro de uma janela e desenha a imagem na posição. Os parâmetros incluem o alça para a janela na qual desenhar a imagem e as coordenadas da posição inicial dentro da janela. As coordenadas são relativas ao canto superior esquerdo da janela, não à área do cliente. O mesmo é verdadeiro para todas as funções de arrastar de imagem que usam coordenadas como parâmetros. Isso significa que você deve compensar as larguras dos elementos da janela, como a borda, a barra de título e a barra de menus ao especificar as coordenadas. Se você especificar um identificador de janela **nulo** ao chamar **ImageList \_ DragEnter**, as funções de arrastar desenharão a imagem no contexto do dispositivo associado à janela da área de trabalho e as coordenadas serão relativas ao canto superior esquerdo da tela.

A função [**ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) cria uma nova imagem de arrastar combinando a imagem determinada (normalmente uma imagem de cursor do mouse) com a imagem de arrastar atual. Como as funções de arrastar usam a nova imagem durante uma operação de arrastar, você deve usar a função de "obter [**cursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) " para ocultar o cursor de mouse real depois de chamar **ImageList \_ SetDragCursorImage**. Caso contrário, o sistema pode parecer ter dois cursores de mouse para a duração da operação de arrastar.

Quando um aplicativo chama [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag), o sistema cria uma lista de imagens temporária e interna e, em seguida, copia a imagem de arrastar especificada para a lista interna. Você pode recuperar o identificador para a lista temporária de imagens de arrastar usando a função [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) . A função também recupera a posição de arrastar atual e o deslocamento da imagem de arrastar em relação à posição de arrastar.

## <a name="image-information"></a>Informações da imagem

Há várias funções que recuperam informações de uma lista de imagens. A função [**ImageList \_ GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) preenche uma estrutura [**IMAGEINFO**](/windows/desktop/api) com informações sobre uma única imagem, incluindo as alças dos bitmaps de imagem e máscara, o número de planos de cores e bits por pixel e o retângulo delimitador da imagem no bitmap de imagem. Você pode usar essas informações para manipular diretamente os bitmaps da imagem. A função [**ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) recupera o número de imagens em uma lista de imagens.

## <a name="image-overlays"></a>Sobreposições de imagem

Cada lista de imagens inclui uma lista de índices a serem usados como sobreposições. Uma sobreposição é uma imagem que é desenhada de forma transparente sobre outra imagem. Qualquer imagem na lista de imagens no momento pode ser usada como uma sobreposição. Você pode especificar até quatro sobreposições por lista de imagens. Esse limite foi expandido para 15 na versão 4,71.

Você adiciona o índice de uma imagem à lista de sobreposições usando a função [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , especificando o identificador para a lista de imagens, o índice da imagem existente e o índice de sobreposição desejado. Isso, na verdade, informa à lista de imagens que "a imagem no índice *x* pode ser usada como uma sobreposição, e quero fazer referência à sobreposição como índice de sobreposição *y*". Os índices de sobreposição são baseados em um, e não em zero, porque um índice de sobreposição igual a zero significa que nenhuma sobreposição será usada.

Você especifica uma sobreposição ao desenhar uma imagem com a função [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) ou [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . A sobreposição é especificada executando uma operação **or** lógica entre os sinalizadores de desenho desejados e o resultado da macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . A macro **INDEXTOOVERLAYMASK** usa o índice de sobreposição e o formata para inclusão com os sinalizadores para essas funções. Isso irá desenhar a imagem com a sobreposição especificada. O exemplo a seguir demonstra como uma sobreposição é adicionada e especificada ao desenhar a imagem.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Isso irá desenhar a imagem 1 e, em seguida, sobrepor essa imagem com a imagem 0. Como 3 é o índice de sobreposição que você especificou na chamada [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , 3 é colocado na macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) .

## <a name="32-bit-antialiased-icons"></a>Ícones com alias de 32 bits

A suavização é uma técnica para suavizar ou Desfocar bordas nítidas. Isso dá a imagens uma aparência mais natural. as listas de imagens no Windows Vista e Windows 7 dão suporte ao uso de bitmaps e ícones antialias de 32 bits. Os valores de cor usam 24 bits e 8 bits são usados como um canal alfa nos ícones. Para criar uma lista de imagens que possa manipular uma imagem de 32 bits por pixel (BPP), chame a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , passando um sinalizador ILC \_ COLOR32.

Para criar ícones de 32 bits corretamente, crie várias imagens para cada ícone, conforme mostrado na ilustração a seguir.

![ilustração mostrando três tamanhos de ícones para cada uma das três profundidades de cor](images/theme2.png)

-   As três primeiras imagens estão no modo de 16 cores para uso no modo de segurança.
-   Os próximos três ícones são usados no modo de cor 256.
-   Os últimos três ícones têm o canal alfa e podem ser usados somente em sistemas operacionais que executam cores de 24 bits ou mais.
-   A ordem das imagens no formato de ícone é importante. se o pedido estiver errado, as versões mais antigas do Windows funcionarão insatisfatoriamente ao extrair os ícones. A extração dos ícones incorretamente pode causar corrupção de memória e renderização incorreta.
-   as versões anteriores do Windows tinham um limite de recursos de 10 ícones.

> [!Note]  
> Você pode usar ferramentas de terceiros para gerar arquivos de ícone e bitmaps que contêm um canal alfa. Se você usar [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) para carregar um bitmap de 32 bpp que contém alfa, será necessário especificar o \_ sinalizador LR CREATEDIBSECTION.

 

 

 