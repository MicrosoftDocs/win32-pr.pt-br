---
title: Barra de idiomas (serviços de texto)
description: Barra de idiomas
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- TSF (estrutura de serviços de texto), barra de idiomas
- TSF (estrutura de serviços de texto), barra de idiomas
- serviços de texto, barra de idiomas
- barra de idiomas
- TSF (estrutura de serviços de texto), botões
- TSF (estrutura de serviços de texto), botões
- serviços de texto, botões
- TSF (estrutura de serviços de texto), menus
- TSF (estrutura de serviços de texto), menus
- serviços de texto, menus
- estilos de botão
- botões de menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41d64a488406f6eefcff5fef6c11093af00bc5b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369163"
---
# <a name="language-bar-text-services"></a>Barra de idiomas (serviços de texto)

## <a name="implementing-the-language-bar-object"></a>Implementando o objeto de barra de idiomas

Para dar suporte à adição de um item à barra de idiomas, um serviço de texto deve implementar um objeto que dê suporte à interface [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) e um dos elementos de controle [ITfLangBarItem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) . Quando o item é instalado, a barra de idiomas instala um coletor [ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) chamando o [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) do item com a IID \_ ITfLangBarItemSink. O item usa a interface **ITfLangBarItemSink** para notificar a barra de idiomas das alterações, por exemplo, quando o item está oculto, mostrado, habilitado ou desabilitado.

Quatro tipos de itens de barra de idiomas podem ser instalados e cada uma das interfaces necessárias é criada a partir de **ITfLangBarItem**. Os elementos de controle **ITfLangBarItem** a seguir são possíveis.



|               |                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botão        | Um botão de barra de idiomas funciona como um botão de comando, um controle de alternância ou um menu na barra de idiomas. O objeto deve dar suporte à interface ITfLangBarItemButton.                   |
| Balão       | Um balão de barra de idiomas funciona como uma notificação pop-up na barra de idiomas. O objeto deve dar suporte à interface ITfLangBarItemBalloon.                                       |
| Bitmap        | Um bitmap de barra de idiomas funciona como um elemento estático na barra de idiomas que exibe um bitmap. O objeto deve dar suporte à interface ITfLangBarItemBitmap.                       |
| Botão bitmap | Um botão de bitmap de barra de idiomas funciona como um elemento de botão na barra de idiomas que exibe o texto e um bitmap. O objeto deve dar suporte à interface ITfLangBarItemBitmapButton. |



 

## <a name="button-styles"></a>Estilos de botão

Um elemento Button pode funcionar como qualquer um dos seguintes. A função do item de botão é determinada pelos sinalizadores definidos no membro **dwStyle** da estrutura [TF \_ LANGBARITEMINFO](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) no método [ITfLangBarItem:: GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) .



|               |                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botão        | O botão funciona como um botão de comando padrão. Esse estilo de botão é identificado pelo \_ estilo de botão TF bin \_ Style \_ BTN \_ . ITfLangBarItemButton:: OnClick é chamado quando o item é clicado. ITfLangBarItemButton:: InitMenu e ITfLangBarItemButton:: OnMenuSelect não são usados.                                                                                                   |
| Botão de alternância | O botão funciona como um controle de alternância que pode manter um estado clicado, semelhante a uma caixa de seleção. Esse estilo de botão é identificado pelo \_ estilo de alternância TF bin \_ Style \_ BTN \_ . ITfLangBarItemButton:: OnClick é chamado quando o item é clicado. ITfLangBarItemButton:: InitMenu e ITfLangBarItemButton:: OnMenuSelect não são usados.                                                  |
| Menu          | O botão funciona como um menu suspenso. Esse estilo de botão é identificado pelo \_ estilo de menu TF bin \_ Style \_ BTN \_ . ITfLangBarItemButton:: InitMenu é chamado quando o botão é clicado. Quando o usuário seleciona um item no menu, a barra de idiomas chama ITfLangBarItemButton:: OnMenuSelect com o identificador do item de menu selecionado. ITfLangBarItemButton:: OnClick não é usado. |



 

## <a name="implementing-a-menu-button"></a>Implementando um botão de menu

Quando o usuário clica em um botão de menu, a barra de idiomas chama [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu). O item adiciona itens ao menu usando a interface [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) passada para InitMenu.

Para adicionar um submenu ao menu, chame [ITfMenu:: addMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) com o \_ \_ submenu TF LBMENUF. Quando isso é feito, um novo objeto **ITfMenu** que representa o submenu é retornado no parâmetro *PpMenu* de addMenuItem. Esse novo objeto de menu é usado para adicionar itens ao submenu.

Quando o usuário seleciona um item no menu, a barra de idiomas chama [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) com o identificador do item de menu selecionado.

## <a name="adding-items-to-the-language-bar"></a>Adicionando itens à barra de idiomas

Um serviço de texto deve adicionar seus itens à barra de idiomas quando o método [ITfTextInputProcessor:: Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) for chamado e removê-los quando seu [ITfTextInputProcessor::D eactivate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) for chamado.

Para adicionar um item à barra de idiomas, o serviço de texto Obtém uma interface [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) chamando ITfThreadMgr:: QUERYINTERFACE com IID \_ ITfLangBarItemMgr. Em seguida, o serviço de texto chama [ITfLangBarItemMgr:: AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) com o ponteiro para o objeto de item de barra de idiomas.

O serviço de texto deve remover o item quando desativado. O serviço de texto usa a mesma interface **ITfLangBarItemMgr** usada para adicionar os itens ou obter outra instância da interface. Em seguida, o serviço de texto chama [ITfLangBarItemMgr:: RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) com o ponteiro de interface do item a ser removido.

## <a name="extending-system-language-bar-items"></a>Estendendo itens da barra de idiomas do sistema

O TSF fornece a capacidade de adicionar itens de menu a menus de barra de idiomas existentes. Isso permite que um serviço de texto adicione itens ao menu de outro serviço de texto sem precisar adicionar um botão separado à barra de ferramentas. Isso também permite que os itens de menu sejam organizados em grupos lógicos. Por exemplo, um serviço de texto que fornece recursos adicionais para o serviço de texto de fala padrão pode adicionar itens ao menu de serviço de texto de fala em vez de adicionar seu próprio botão de menu de nível superior.

Um serviço de texto fornece uma extensão de menu de barra de idiomas implementando um objeto que dá suporte à interface [ITfSystemLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) . Essa interface funciona exatamente como a interface [ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) para um botão de menu. Quando o menu é exibido, o serviço de texto que está sendo estendido chama [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu). A extensão adiciona itens ao menu usando a interface [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) passada para **InitMenu**. Quando o usuário seleciona um item adicionado pela extensão, o serviço de texto que está sendo estendido chama [ITfSystemLangBarItemSink:: OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) com o identificador do item de menu selecionado.

Para instalar uma extensão de menu da barra de idiomas, o serviço de texto conclui as etapas a seguir.

1.  Obtenha a interface **ITfLangBarItem** para o item a ser estendido chamando [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) com o **GUID** para o item a ser estendido.
2.  Obtenha a interface **ITfSource** para o item a ser estendido chamando ITfLangBarItem:: QUERYINTERFACE com IID \_ ITfSource.
3.  Chame [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfSystemLangBarItemSink e o ponteiro para o objeto **ITfSystemLangBarItemSink** . Se ITfSource:: AdviseSink falhar, o serviço de texto não oferece suporte a extensões de menu.

[ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource:: AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Suporte a extensões de menu da barra de idiomas

Um serviço de texto pode permitir que outros serviços de texto adicionem itens aos seus menus da barra de idiomas, conforme mostrado acima. O serviço de texto que deve publicar seu GUID para que o item possa ser obtido chamando [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem).

Para dar suporte a extensões de menu, o serviço de texto deve dar suporte à interface [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) . As etapas a seguir habilitam o suporte para uma ou mais extensões de menu.

1.  Quando [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfSystemLangBarItemSink é chamado, o serviço de texto deve armazenar a interface **ITfSystemLangBarItemSink** e retornar um valor de cookie que identificará a extensão.
2.  Quando [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) é chamado, o serviço de texto chama o método [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) da extensão. O serviço de texto deve implementar uma maneira de identificar os itens de menu adicionados pela extensão, em oposição aos itens adicionados pelo próprio serviço de texto.
3.  Quando [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) é chamado com um identificador de item de menu que pertence a uma extensão, o serviço de texto chama o método **ITfSystemLangBarItemSink:: OnMenuSelect** de extensões.
4.  Quando [ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) é chamado com o cookie apropriado, o serviço de texto remove a extensão do menu.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como configurar a estrutura de serviços de texto](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de idiomas (aplicativos)](language-bar-app.md)
</dt> </dl>

 

 
