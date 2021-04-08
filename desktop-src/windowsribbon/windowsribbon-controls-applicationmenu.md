---
title: Menu do aplicativo
description: O menu aplicativo é o menu principal para um aplicativo que implementa a estrutura da faixa de dasgem do Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823775"
---
# <a name="application-menu"></a>Menu do aplicativo

O menu aplicativo é o menu principal para um aplicativo que implementa a estrutura da faixa de dasgem do Windows.

-   [Introdução](#introduction)
-   [Componentes do menu do aplicativo](#components-of-the-application-menu)
    -   [Menu de menus do aplicativo](#application-menu-menugroup)
-   [Dimensionando o menu do aplicativo](#sizing-the-application-menu)
-   [Propriedades do menu do aplicativo](#application-menu-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O menu do aplicativo é composto por um controle de botão suspenso que exibe um menu contendo comandos que expõem a funcionalidade relacionada a um projeto completo, como um documento, imagem ou filme inteiro. Os exemplos incluem os comandos **novo**, **abrir**, **salvar** e **sair** .

A captura de tela a seguir ilustra o menu do aplicativo.

![captura de tela da lista de menus do aplicativo e itens recentes da faixa de pintura do Paint para Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Componentes do menu do aplicativo

O menu aplicativo é um elemento obrigatório em qualquer aplicativo da faixa de faixas. O ponto de entrada no menu do aplicativo é um botão distintivo que aparece como o primeiro item na linha da [guia](windowsribbon-controls-tab.md) , conforme mostrado na captura de tela a seguir.

> [!Note]  
> Windows 8 e mais recente: imagem do botão de menu do aplicativo alterada para rótulo: **arquivo**. Recomendamos que você não use o arquivo como rótulo para qualquer uma das suas próprias guias.

 

![captura de tela do botão de menu do aplicativo do WordPad para Windows 7.](images/overviews/applicationmenu-button.png)

Quando clicado, esse botão exibe o menu avançado que é mostrado na captura de tela a seguir (o menu do aplicativo do WordPad para Windows 7).

![captura de tela do menu de menu do aplicativo do WordPad para Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> Não há nenhum impacto no conjunto de guias quando o botão de menu do aplicativo é clicado; em vez disso, o foco entra no menu.

 

O menu aplicativo contém dois painéis: uma lista de comandos representados por um ou mais elementos do [**menu de menus**](windowsribbon-element-menugroup.md) e uma lista de [itens recentes](windowsribbon-controls-recentitems.md) representada por um elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

### <a name="application-menu-menugroup"></a>Menu de menus do aplicativo

O elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) deve conter pelo menos um elemento filho de um [**menu**](windowsribbon-element-menugroup.md) que expõe uma lista de comandos no nível do aplicativo. Se vários elementos do grupo de **menus** forem declarados, uma linha divisória será desenhada entre os grupos, conforme mostrado na captura de tela a seguir.

![captura de tela de um menu de menu do aplicativo.](images/overviews/applicationmenu-menugroup.png)

Veja a seguir uma lista de restrições para um elemento do [**menu**](windowsribbon-element-menugroup.md) de um do menu do aplicativo:

-   Todos os itens do [**menu de menus**](windowsribbon-element-menugroup.md) devem ser declarados com um valor de atributo de *classe* de `MajorItems` .
-   Um  [**menu de aplicativo é compatível apenas**](windowsribbon-element-menugroup.md) com o [botão](windowsribbon-controls-button.md), [botão de alternância](windowsribbon-controls-togglebutton.md), botão [suspenso](windowsribbon-controls-dropdownbutton.md), [botão de divisão](windowsribbon-controls-splitbutton.md), [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)e controles de [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) .
    > \[! Fundamental\]  
    > As galerias de comandos são o único tipo de galeria com suporte no menu do aplicativo. Consulte [trabalhando com galerias](./ribbon-controls-galleries.md)para obter mais informações sobre controles da galeria.

     

Quando um [botão](windowsribbon-controls-button.md) ou [botão de alternância](windowsribbon-controls-togglebutton.md) é usado em um [**menu**](windowsribbon-element-menugroup.md), o valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) é exibido no menu e os valores de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) e [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) são exibidos como a dica de ferramenta, conforme mostrado na captura de tela a seguir.

![captura de tela de um controle de botão em um menu de aplicativo.](images/overviews/applicationmenu-menubutton.png)

Quando um [botão suspenso](windowsribbon-controls-dropdownbutton.md), um [botão de divisão](windowsribbon-controls-splitbutton.md), uma [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)ou uma [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) são usados no menu do aplicativo, a parte do menu é exibida como um submenu que cobre e oculta o painel **itens recentes** .

Para os controles botão de [divisão](windowsribbon-controls-splitbutton.md) e [botão suspenso](windowsribbon-controls-dropdownbutton.md) , o valor de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) é mostrado embutido no menu do submenu para auxiliar visualmente os usuários com a descoberta da funcionalidade do comando. O valor exibido de **Command. LabelDescription** é interrompido programaticamente em um intervalo de duas linhas e é feita uma tentativa de ajustar o valor exatamente acima do painel **itens recentes** abaixo. Se o valor de **Command. LabelDescription** não couber, o submenu será expandido para acomodar o valor de comando mais longo [**. Comment**](windowsribbon-element-command-comment.md) no [**menu**](windowsribbon-element-menugroup.md).

A captura de tela a seguir ilustra esses comportamentos em um submenu de [botão de divisão](windowsribbon-controls-splitbutton.md) .

![captura de tela de um submenu de controle de lista em um menu de aplicativo.](images/overviews/applicationmenu-menuflyout.png)

Com uma [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) e uma galeria de [botões de divisão](windowsribbon-controls-splitbuttongallery.md), apenas um rótulo e uma imagem são mostrados.

## <a name="sizing-the-application-menu"></a>Dimensionando o menu do aplicativo

O dimensionamento do menu do aplicativo é tratado pela estrutura da faixa de faixas. Se forem fornecidas cadeias de caracteres muito longas para o valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), ou se uma longa lista de comandos for usada, o menu ajustará seu tamanho para acomodar o conteúdo. Algumas formas de ajuste incluem expandir o tamanho de submenus ou painéis de menus e adicionar visualizadores de Pan quando a rolagem é necessária.

## <a name="application-menu-properties"></a>Propriedades do menu do aplicativo

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de menu do aplicativo.

Normalmente, uma propriedade de menu de aplicativo é atualizada na interface do usuário da faixa de guia invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo não é consultado quanto a um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, a estrutura requer a propriedade quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de ferramentas ou quando uma dica de ferramenta é exibida.



| Chave de propriedade                                                                                     | Observações                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação. |
| [\_TooltipTitle PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação ApplicationMenu**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 