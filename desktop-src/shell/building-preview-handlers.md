---
description: Este tópico discute as interfaces e os métodos específicos necessários para criar um Gerenciador de visualização.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Criando gerenciadores de visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296219"
---
# <a name="building-preview-handlers"></a>Criando gerenciadores de visualização

Este tópico discute as interfaces e os métodos específicos necessários para criar um Gerenciador de visualização.

Um Gerenciador de visualização deve implementar as seguintes interfaces:

-   [IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (altamente preferencial), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)ou [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Se o seu Gerenciador de visualização oferecer suporte a configurações visuais fornecidas pelo host, como cor e fonte do plano de fundo, ele também deverá implementar a seguinte interface:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

Este tópico pressupõe que o Gerenciador de visualização seja inicializado com um fluxo e seja registrado para uma extensão de nome de arquivo específica.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream:: Initialize

Armazene os parâmetros de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) e de modo para que você possa ler os dados do item quando estiver pronto para visualizar o item. Não carregue os dados na [**inicialização**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Carregue os dados em [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) antes de renderizar.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite:: SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite:: GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite:: SetSite

Armazene o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para acesso posterior.

Se, no momento, você tiver uma referência a um objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , libere-o. Use o ponteiro de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) armazenado para chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para uma nova referência de **IPreviewHandlerFrame** .

Se você tiver uma tabela de acelerador, destrua-a. Chame [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) para obter uma nova tabela de acelerador. Armazene esta tabela. Observe que ele é usado apenas como uma lista de teclas de aceleração com suporte no quadro. Os comandos nas entradas do acelerador são ignorados.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite:: GetSite

Retorne o ponteiro do site, seja qual for.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow:: GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Retornar E \_ NOTIMPL para este método.

### <a name="iolewindowgetwindow"></a>IOleWindow:: GetWindow

Se a janela do Gerenciador de visualização existir no momento, retorne o **HWND** dessa janela e s \_ OK. Se a janela não existir, retornará E \_ falhará.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler:: SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler:: SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler:: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler:: QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler:: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler:: Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler:: SetWindow

Defina o parâmetro *HWND* deste método como o pai do **HWND** do Gerenciador de visualização. Esse método pode ser chamado várias vezes. Redimensione sua visualização para que ela seja renderizada apenas na área descrita pelo parâmetro *prc* .

Se o previsor estiver no processo de renderização, use o método [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) para alterar o pai do pré-visor. Altere também a área na qual o previsor está renderizando.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler:: SetRect

Redimensione sua visualização para que ela seja renderizada apenas na área descrita pelo *prc* desse método.

Se o previsor estiver no processo de renderização, altere a área em que o seu visualizador é renderizado.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

É aí que o trabalho real é feito. Como uma visualização é dinâmica, o conteúdo da visualização só deve ser carregado quando necessário. Não carregue o conteúdo na inicialização.

Se a janela do Gerenciador de visualização não existir, crie-a. As janelas do Gerenciador de visualização devem ser filhas da janela fornecida por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Eles devem ter o tamanho fornecido por **IPreviewHandler:: SetWindow** e [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (o que foi chamado mais recentemente).

Quando você tiver uma janela, carregue os dados do [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) com o qual o Gerenciador de visualização foi inicializado e os processe para a janela do seu Gerenciador de visualização.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler:: SetFocus

Esse método é chamado quando o foco entra no painel de leitura por meio de uma ação de guia. Como ele pode ser inserido como uma guia avançar ou uma guia reversa, use o estado atual da tecla SHIFT para decidir se a primeira ou última parada de tabulação no painel de leitura deve receber o foco.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler:: QueryFocus

Esse método deve chamar a função [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) e retornar o resultado dessa chamada no parâmetro *phwnd* .

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler:: TranslateAccelerator

Esse método é chamado pelo bombeamento da mensagem do processo do Gerenciador de visualização (se prevhost.exe ou um servidor local personalizado) em resposta a pressionamentos de tecla do usuário. Os gerenciadores de visualização devem lidar com esses pressionamentos de teclas ou encaminhá-los ao host de acordo com o algoritmo detalhado abaixo.

No entanto, como as visualizações são somente leitura, a entrada do teclado deve ser mínima e otimizações como essa não são necessárias em muitos casos.

Se o acelerador de teclado passado para esse método por meio da bomba de mensagem for um acelerador que o seu Gerenciador de visualização aceitará, processe-o e retorne os S \_ OK. Se o manipulador não aceitar esse acelerador, a mensagem do acelerador poderá ser enviada de volta até o quadro a ser manipulado.

Há duas opções para encaminhar aceleradores de teclado de volta ao quadro:

O modelo mais simples é encaminhar todos os pressionamentos de tecla para o host usando [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Isso é feito no exemplo do Gerenciador de visualização fornecido com o SDK (Software Development Kit) do Windows. Todos os gerenciadores de visualização de baixa integridade devem usar esse modelo. Se o acelerador não for tratado pelo seu Gerenciador de visualização, chame **IPreviewHandlerFrame:: TranslateAccelerator** e retorne seu resultado.

O outro modelo é usar uma tabela de acelerador como uma otimização para evitar o envio de muitos pressionamentos de tecla entre limites de processo:

1.  Quando [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) é chamado no seu Gerenciador de visualização, adquira a tabela de acelerador por meio de [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Certifique-se de liberar o identificador para a tabela de aceleração quando o seu visualizador for destruído.)
2.  Se o acelerador for manipulado pelo seu Gerenciador de visualização, manipule-o e retorne os S \_ OK.
3.  Se o acelerador não for manipulado pelo seu Gerenciador de visualização, compare a mensagem usando [**isaccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) com base na tabela de aceleração adquirida.
4.  Se o acelerador corresponder a uma entrada nessa tabela de acelerador, chame [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) e retorne seu resultado.
5.  Se o acelerador não corresponder a nenhuma entrada na tabela do acelerador, retornará S \_ false.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler:: Unload

Quando esse método é chamado, pare qualquer renderização, libere todos os recursos alocados lendo dados do fluxo e libere o [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) em si.

Depois que esse método é chamado, o manipulador deve ser reinicializado antes de qualquer tentativa de chamar [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) novamente.

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals:: setBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals:: SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Esses métodos devem ser implementados ao direcionar o Gerenciador de visualização para responder aos esquemas de cores e fontes do host. O host consulta o manipulador para [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). Se houver suporte, o host o fornecerá com cores, fontes e cor do texto.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals:: setBackgroundColor

Armazene essa cor e use-a durante a renderização quando desejar fornecer uma cor de plano de fundo. Por exemplo, para preencher a janela quando o manipulador é renderizado para uma área menor do que a área fornecida por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) e [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Observe, no entanto, que você não deve desenhar fora da área fornecida por esses métodos.

Se esse método for chamado enquanto a visualização já estiver sendo processada, a renderização deverá ser reiniciada usando essa cor de plano de fundo.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals:: SetFont

Armazene essas informações de fonte e use-as durante a renderização quando desejar exibir texto consistente com as configurações atuais do Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

Armazene essas informações de cor do texto e use-as durante a renderização quando desejar exibir texto consistente com as configurações atuais do Windows Vista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciadores de visualização e host de visualização do Shell](preview-handlers.md)
</dt> <dt>

[Como registrar um Gerenciador de visualização](how-to-register-a-preview-handler.md)
</dt> <dt>

[Diretrizes do Gerenciador de visualização](preview-handler-guidelines.md)
</dt> </dl>

 

 
