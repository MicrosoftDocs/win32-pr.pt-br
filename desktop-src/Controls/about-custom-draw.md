---
title: Sobre o desenho personalizado
description: Esta seção contém informações gerais sobre a funcionalidade de desenho Personalizada e fornece uma visão geral conceitual de como um aplicativo pode dar suporte a desenho personalizado.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4961d80c04f8fa570286666511c04b1208c940369cd13b836095b8899505de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922486"
---
# <a name="about-custom-draw"></a>Sobre o desenho personalizado

Esta seção contém informações gerais sobre a funcionalidade de desenho Personalizada e fornece uma visão geral conceitual de como um aplicativo pode dar suporte a desenho personalizado. Atualmente, os seguintes controles oferecem suporte à funcionalidade de desenho Personalizada:

-   Controles de cabeçalho
-   Controles de exibição de lista
-   Controles Rebar
-   Controles da barra de ferramentas
-   Controles de dica de ferramenta
-   Controles TrackBar
-   Controles de exibição de árvore

<!-- -->

-   [Sobre as mensagens de notificação de desenho personalizado](#about-custom-draw-notification-messages)
-   [Paint Ciclos, estágios de desenho e mensagens de notificação](#paint-cycles-drawing-stages-and-notification-messages)
-   [Aproveitando os serviços personalizados de desenho](#taking-advantage-of-custom-draw-services)
    -   [Respondendo à notificação de prepintura](#responding-to-the-prepaint-notification)
    -   [Solicitando notificações específicas do item](#requesting-item-specific-notifications)
    -   [Desenhando o item por conta própria](#drawing-the-item-yourself)
    -   [Alterando fontes e cores](#changing-fonts-and-colors)
-   [Desenho personalizado com controles List-View e Tree-View](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Desenho personalizado com controles de List-View](#custom-draw-with-list-view-controls)
-   [Tópicos relacionados](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Sobre as mensagens de notificação de desenho personalizado

Todos os controles comuns que dão suporte a códigos de notificação [ \_ CUSTOMDRAW](nm-customdraw.md) de envio do nm e personalizados em pontos específicos durante operações de desenho. Esses códigos de notificação descrevem as operações de desenho que se aplicam ao controle inteiro, bem como o desenho de operações específicas a itens dentro do controle. Como muitos códigos de notificação, \_ as notificações nm CUSTOMDRAW são enviadas como mensagens de [**\_ notificação do WM**](wm-notify.md) .

O parâmetro *lParam* de uma notificação de desenho Personalizada será o endereço de uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) ou de uma estrutura específica de controle que contém uma estrutura **NMCUSTOMDRAW** como seu primeiro membro. A tabela a seguir ilustra a relação entre os controles e as estruturas que eles usam.



| Estrutura                                | Usado por                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Controles Rebar, TrackBar e header |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Controles de exibição de lista                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Controles da barra de ferramentas                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Controles de dica de ferramenta                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Controles de exibição de árvore                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Paint Ciclos, estágios de desenho e mensagens de notificação

assim como todos os aplicativos Windows, os controles comuns pintam e apagam-se periodicamente com base nas mensagens recebidas do sistema ou de outros aplicativos. O processo de uma pintura de controle ou apagamento é chamado de *ciclo de pintura*. Controles que dão suporte a códigos de notificação [ \_ CUSTOMDRAW](nm-customdraw.md) de envio de nm para desenho personalizado periodicamente por meio de cada ciclo de pintura. Esse código de notificação é acompanhado por uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) ou outra estrutura que contém uma estrutura **NMCUSTOMDRAW** como seu primeiro membro.

Uma informação que a estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contém é o estágio atual do ciclo de pintura. Isso é chamado de estágio de *desenho* e é representado pelo valor no membro **dwDrawStage** da estrutura. Um controle informa seu pai sobre quatro estágios básicos de desenho. Esses estágios básico, ou global, de desenho são representados na estrutura pelos seguintes valores de sinalizador (definidos em commctrl. h).



| Valores de estágio de desenho global | Descrição                        |
|--------------------------|------------------------------------|
| CDDS \_ PREpaint           | Antes do início do ciclo de pintura.     |
| CDDS \_          | Após a conclusão do ciclo de pintura. |
| CDDS de \_ PREborracha           | Antes do início do ciclo de apagamento.     |
| CDDS de \_ apagamento          | Após a conclusão do ciclo de apagamento. |



 

Cada um dos valores anteriores pode ser combinado com o \_ sinalizador de item CDDs para especificar estágios de desenho específicos de itens. Para sua conveniência, commctrl. h contém os valores específicos de item a seguir.



| Valores de estágio de desenho específicos do item | Descrição                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDS \_ ITEMPREPAINT              | Antes de um item ser desenhado.                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | Depois que um item foi desenhado.                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | Antes de um item ser apagado.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Depois que um item foi apagado.                                                                                                                                                                                                                                                      |
| subitem CDDS \_                   | [Versões de controle comuns](common-control-versions.md) 4,71. Sinalizador combinado com CDDS \_ ITEMPREPAINT ou CDDs \_ ITEMPOSTPAINT se um subitem estiver sendo desenhado. Isso só será definido se [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) for retornado de CDDs \_ PrePaint. |



 

Seu aplicativo deve processar o código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) e retornar um valor específico que informará ao controle o que ele deve fazer. Consulte as seções a seguir para obter mais informações sobre esses valores de retorno.

## <a name="taking-advantage-of-custom-draw-services"></a>Aproveitando os serviços personalizados de desenho

A chave para o aproveitamento da funcionalidade de desenho Personalizada é responder aos códigos de notificação do [nm \_ CUSTOMDRAW](nm-customdraw.md) que um controle envia. Os valores de retorno que seu aplicativo envia em resposta a essas notificações determinam o comportamento do controle para esse ciclo de pintura.

Esta seção contém informações sobre como seu aplicativo pode usar os valores de retorno de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) para determinar o comportamento do controle.

Os detalhes são divididos nos seguintes tópicos:

-   [Respondendo à notificação de prepintura](#responding-to-the-prepaint-notification)
-   [Solicitando notificações específicas do item](#requesting-item-specific-notifications)
-   [Desenhando o item por conta própria](#drawing-the-item-yourself)
-   [Alterando fontes e cores](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Respondendo à notificação de prepintura

No início de cada ciclo de pintura, o controle envia o código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) , especificando o \_ valor de CDDs PrePaint no membro **dwDrawStage** da estrutura nm CUSTOMDRAW que o acompanha \_ . O valor que seu aplicativo retorna para essa primeira notificação determina como e quando o controle envia notificações de desenho personalizadas subsequentes para o restante desse ciclo de pintura. Seu aplicativo pode retornar uma combinação dos sinalizadores a seguir em resposta à primeira notificação.



| Valor retornado            | Efeito                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dopadrão CDRF \_         | O controle será desenhado em si mesmo. Ele não enviará notificações [de \_ CUSTOMDRAW nm](nm-customdraw.md) adicionais para este ciclo de pintura. Esse sinalizador não pode ser usado com nenhum outro sinalizador.                                                                                                                                                                                                                                                                               |
| doborracha CDRF \_           | O controle só desenhará o plano de fundo.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](#changing-fonts-and-colors). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | O controle notificará o pai de qualquer operação de desenho específica de item. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de desenhar os itens. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | O controle enviará uma notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) quando o ciclo de pintura de todo o controle for concluído. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Versão 4,71](common-control-versions.md). Seu aplicativo receberá uma notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT \| CDDs \_ subitem antes de cada subitem de exibição de lista ser desenhado. Em seguida, você pode especificar a fonte e a cor de cada subitem separadamente ou retornar [**CDRF \_ DODEFAULT**](cdrf-constants.md) para processamento padrão. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT. |
| CDRF \_ SKIPDEFAULT       | Seu aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | O controle não desenhará o retângulo de foco em um item.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Solicitando notificações específicas do item

Se seu aplicativo retornar [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) à notificação de desenho personalizado pretinta inicial, o controle enviará notificações para cada item que ele desenha durante esse ciclo de pintura. Essas notificações específicas de item terão o valor CDDS \_ ITEMPREPAINT no membro **dwDrawStage** da estrutura de [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que o acompanha. Você pode solicitar que o controle envie outra notificação quando terminar de desenhar o item, retornando [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) a essas notificações específicas de item. Caso contrário, [**retornará \_ DODEFAULT CDRF**](cdrf-constants.md) e o controle não notificará a janela pai até que comece a desenhar o próximo item.

### <a name="drawing-the-item-yourself"></a>Desenhando o item por conta própria

Se seu aplicativo desenha o item inteiro, retorne [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md). Isso permite que o controle ignore itens que não precisam ser desenhados, diminuindo assim a sobrecarga do sistema. Tenha em mente que retornar esse valor significa que o controle não desenhará nenhuma parte do item.

### <a name="changing-fonts-and-colors"></a>Alterando fontes e cores

Seu aplicativo pode usar o Draw personalizado para alterar a fonte de um item. Basta selecionar o HFONT que você deseja no contexto do dispositivo especificado pelo membro **HDC** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada à notificação de desenho Personalizada. Como a fonte selecionada pode ter métricas diferentes da fonte padrão, certifique-se de incluir o [**CDRF \_ NEWFONT**](cdrf-constants.md) bit no valor de retorno para a mensagem de notificação. Para obter mais informações sobre como usar essa funcionalidade, consulte o código de exemplo em [usando o desenho personalizado](using-custom-draw.md). A fonte que seu aplicativo especifica é usada para exibir esse item quando ele não está selecionado. O desenho personalizado não permite que você altere os atributos de fonte dos itens selecionados.

Para alterar as cores do texto de todos os controles que dão suporte a desenho personalizado, exceto para exibição de lista e exibição de árvore, basta definir o texto desejado e as cores do plano de fundo no contexto do dispositivo fornecido na estrutura de notificação de desenho personalizada com as funções [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) e [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) . Para modificar as cores do texto no modo de exibição de lista ou de árvore, você precisa posicionar os valores de cor desejados nos membros **clrText** e **ClrTextBk** da estrutura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) ou [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) .

> [!Note]  
> Antes da [versão 6,0](common-control-versions.md) dos controles comuns, as barras de ferramentas ignoram o sinalizador [**CDRF \_ NEWFONT**](cdrf-constants.md) . A versão 6,0 dá suporte ao sinalizador **CDRF \_ NEWFONT** e você pode usá-lo para selecionar uma fonte diferente para a barra de ferramentas. No entanto, você não pode alterar a cor de uma barra de ferramentas quando um estilo visual está ativo. Para alterar a cor de uma barra de ferramentas na versão 6,0, primeiro você deve desabilitar os estilos visuais chamando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) e especificando nenhum estilo visual:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Desenho personalizado com controles List-View e Tree-View

Os controles mais comuns podem ser manipulados essencialmente da mesma forma. No entanto, os controles List-View e Tree-View têm alguns recursos que exigem uma abordagem um pouco diferente do desenho personalizado.

Para a [versão 5,0](common-control-versions.md), esses dois controles podem exibir texto recortado se você alterar a fonte retornando [**CDRF \_ NEWFONT**](cdrf-constants.md). Esse comportamento é necessário para compatibilidade com versões anteriores dos controles comuns. Se você quiser alterar a fonte de um modo de exibição de lista ou de exibição de árvore, obterá resultados melhores se enviar uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com o valor *wParam* definido como 5 antes de adicionar qualquer item ao controle. Para obter um exemplo de um controle de exibição de árvore que usa desenho personalizado, consulte o artigo da base de dados de conhecimento [exemplo: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Desenho personalizado com controles de List-View

Como os controles de exibição de lista têm subitens e vários modos de exibição, você precisará manipular a notificação do [nm \_ CUSTOMDRAW](nm-customdraw.md) um pouco diferente do que para os outros controles comuns.

Para o modo de relatório, use o procedimento a seguir.

1.  A primeira notificação de [ \_ CUSTOMDRAW nm](nm-customdraw.md) terá o membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada definida como CDDs \_ PrePaint. Retornar [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Em seguida, você receberá uma notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT. Se você especificar novas fontes ou cores e retornar [**CDRF \_ NEWFONT**](cdrf-constants.md), todos os subitens do item serão alterados. Se desejar, em vez disso, manipular cada subitem separadamente, retorne [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Se você retornou [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) na etapa anterior, receberá uma notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) para cada SUBitem com **dwDrawStage** definido como CDDs \_ subitem CDDs \| \_ ITEMPREPAINT. Para alterar a fonte ou a cor do subitem, especifique uma nova fonte ou cor e retorne [**CDRF \_ NEWFONT**](cdrf-constants.md).

Para os modos de ícone grande, ícone pequeno e lista, use o procedimento a seguir.

1.  A primeira notificação de [ \_ CUSTOMDRAW nm](nm-customdraw.md) terá o membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada definida como CDDs \_ PrePaint. Retornar [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Em seguida, você receberá uma notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT. Você pode alterar as fontes ou cores de um item especificando novas fontes e cores e retornando [**CDRF \_ NEWFONT**](cdrf-constants.md). Como esses modos não têm subitens, você não receberá nenhuma notificação de CUSTOMDRAW NM adicional \_ .

Para obter um exemplo de um manipulador de notificação de [ \_ CUSTOMDRAW nm](nm-customdraw.md) de exibição de lista, consulte [usando o desenho personalizado](using-custom-draw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Usando o desenho personalizado](using-custom-draw.md)
</dt> <dt>

[Referência de desenho Personalizada](custom-draw-reference.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[EXEMPLO: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 