---
description: O controle InkEdit permite que você colete tinta, reconheça a tinta e exiba a tinta como texto.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Referência de controle InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53edfdc6a72a7792c60a6c7c7bf0e38ffc5e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011687"
---
# <a name="inkedit-control-reference"></a>Referência de controle InkEdit

O controle InkEdit permite que você colete tinta, reconheça a tinta e exiba a tinta como texto. Esse controle permite que você habilite formulários inteligentes, o que melhora a precisão da entrada de texto.

Esse controle é um superconjunto do controle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Ele estende o controle **RichEdit** com a capacidade de capturar, reconhecer e exibir tinta.

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

A criação do controle InkEdit por trás de um controle transparente (como uma caixa de grupo com o conjunto de propriedades de WS \_ ex \_ Transparent) impedirá InkEdit de coletar tinta.

## <a name="members"></a>Membros



| Enumeração                                            | Descrição                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Define os valores que especificam se o controle parece simples ou 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Define os valores que especificam se o controle tem uma borda.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Define os valores que definem o interesse em um conjunto de gestos específicos do aplicativo.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Define valores que especificam se uma seleção aparece como tinta ou texto.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Define valores que especificam se o controle InkEdit está ocioso, coletando tinta ou reconhecendo tinta.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Define os valores que especificam como a tinta é inserida no controle InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Define os valores que especificam as configurações do modo de coleta para tinta desenhada-se a coleta de tinta está desabilitada, a tinta é coletada ou a tinta e os gestos são coletados.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Define os valores que especificam qual botão do mouse foi pressionado.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Define os valores que especificam o tipo de ponteiro do mouse que aparece.<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Define os valores que especificam qual botão do mouse foi pressionado.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Define os valores que especificam como as barras de rolagem de um controle InkEdit aparecem na tela.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Define os valores que especificam o alinhamento do parágrafo em relação às margens do controle InkEdit.<br/>                                                      |



 



| Mensagem de notificação de eventos                                   | Descrição                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [IECN \_ traço](inkedit-messages--win32-only-.md)            | Essa mensagem é enviada por meio de uma \_ mensagem de notificação do WM quando um traço é concluído (somente Win32).<br/>  |
| [gesto de IECN \_](inkedit-messages--win32-only-.md)           | Essa mensagem é enviada por meio de uma \_ mensagem de notificação do WM quando um gesto é concluído (somente Win32).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Essa mensagem é enviada por meio de uma \_ mensagem de notificação do WM quando ocorre reconhecimento (somente Win32).<br/>     |



 



| Evento                                                  | Descrição                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Alteração**](inkedit-change.md)                       | Ocorre quando o conteúdo do controle ou um valor de propriedade é alterado.<br/>                                                                                                              |
| [**Clicar**](inkedit-click.md)                         | Ocorre quando um usuário clica no controle.<br/>                                                                                                                                              |
| [**DblClick**](inkedit-dblclick.md)                   | Ocorre quando um usuário clica duas vezes no controle.<br/>                                                                                                                                       |
| [**Gesto**](inkedit-gesture.md)                     | Ocorre quando um gesto de aplicativo é reconhecido.<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | Ocorre quando o usuário pressiona uma tecla enquanto o controle InkEdit tem foco.<br/>                                                                                                          |
| [**Pressionar**](inkedit-keypress.md)                   | Ocorre quando uma tecla é pressionada enquanto o controle InkEdit tem foco.<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | Ocorre quando uma tecla é liberada enquanto o controle InkEdit tem foco.<br/>                                                                                                               |
| [**MouseDown**](inkedit-mousedown.md)                 | Ocorre quando o ponteiro do mouse está sobre o controle InkEdit e um botão do mouse é pressionado.<br/>                                                                                         |
| [**Ocorra**](inkedit-mousemove.md)                 | Ocorre quando o ponteiro do mouse é movido sobre o controle InkEdit.<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | Ocorre quando o ponteiro do mouse está sobre o controle InkEdit e um botão do mouse é liberado.<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | Ocorre quando o controle InkEdit Obtém os resultados manualmente de uma chamada para o método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automaticamente após o tempo limite do reconhecimento ser acionado.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Ocorre quando a seleção de tinta dentro do controle InkEdit é alterada.<br/>                                                                                                             |
| [**Pincel**](inkedit-stroke.md)                       | Ocorre quando o usuário desenha um novo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em qualquer objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .<br/>                                                 |



 



| Obter/definir mensagem                                               | Descrição                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [em \_ GETINKMODE](inkedit-messages--win32-only-.md)           | Obtém o modo de tinta do controle (somente Win32).<br/>                                                                                                                       |
| [em \_ SETINKMODE](inkedit-messages--win32-only-.md)           | Define o modo de tinta do controle (somente Win32).<br/>                                                                                                                       |
| [em \_ GETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Obtém o modo de inserção de tinta do controle (somente Win32).<br/>                                                                                                             |
| [em \_ SETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Define o modo de inserção de tinta do controle (somente Win32).<br/>                                                                                                             |
| [em \_ GETDRAWATTR](inkedit-messages--win32-only-.md)          | Obtém os atributos de desenho atuais do controle (somente Win32).<br/>                                                                                                     |
| [em \_ SETDRAWATTR](inkedit-messages--win32-only-.md)          | Define os atributos de desenho a serem usados para a coleta de tinta futura (somente Win32).<br/>                                                                                           |
| [em \_ GETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Obtém o tempo limite de reconhecimento para o controle (somente Win32).<br/>                                                                                                           |
| [em \_ SETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Define o tempo limite de reconhecimento para o controle (somente Win32).<br/>                                                                                                           |
| [em \_ GETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Obtém o status do gesto para o controle (somente Win32).<br/>                                                                                                                |
| [em \_ SETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Define o status do gesto para o controle (somente Win32).<br/>                                                                                                                |
| [em \_ GETcognizer](inkedit-messages--win32-only-.md)        | Obtém o reconhecedor usado pelo controle (somente Win32).<br/>                                                                                                              |
| [em \_ Recognizer](inkedit-messages--win32-only-.md)        | Define o reconhecedor usado pelo controle (somente Win32).<br/>                                                                                                              |
| [em \_ GETfactoid](inkedit-messages--win32-only-.md)           | Obtém o factor a ser usado para reconhecimento (somente Win32).<br/>                                                                                                                |
| [em \_ SETFACTIOD](inkedit-messages--win32-only-.md)           | Define o factor a ser usado para reconhecimento (somente Win32).<br/>                                                                                                                |
| [em \_ GETSELINK](inkedit-messages--win32-only-.md)            | Obtém a tinta na seleção (somente Win32).<br/>                                                                                                                          |
| [em \_ SETSELINK](inkedit-messages--win32-only-.md)            | Define a tinta na seleção (somente Win32).<br/>                                                                                                                          |
| [em \_ GETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Retorna a aparência atual da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (somente Win32).<br/> |
| [em \_ SETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Define a aparência da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (somente Win32).<br/>            |
| [em \_ GETstatus](inkedit-messages--win32-only-.md)            | Obtém o status do controle (somente Win32).<br/>                                                                                                                         |
| [\_Recognize](inkedit-messages--win32-only-.md)            | Força o reconhecimento (somente Win32).<br/>                                                                                                                                     |
| [em \_ GETMOUSEICON](inkedit-messages--win32-only-.md)         | Obtém o ícone do mouse (somente Win32).<br/>                                                                                                                                    |
| [em \_ SETMOUSEICON](inkedit-messages--win32-only-.md)         | Define o ícone do mouse (somente Win32).<br/>                                                                                                                                    |
| [em \_ GETmousepointer](inkedit-messages--win32-only-.md)      | Obtém o ponteiro do mouse (somente Win32).<br/>                                                                                                                                 |
| [em \_ SETmousepointer](inkedit-messages--win32-only-.md)      | Define apenas o ponteiro do mouse em Win32).<br/>                                                                                                                                  |
| [em \_ GETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Obtém o estado de se a entrada do mouse é tratada como entrada de caneta (somente Win32).<br/>                                                                                        |
| [em \_ SETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Define o estado de se a entrada do mouse é tratada como entrada à caneta (somente Win32).<br/>                                                                                        |



 



| Método                                               | Descrição                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Obtém o interesse do controle InkEdit em um conjunto conhecido de gestos.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Especifica que o reconhecimento deve ocorrer.<br/>                             |
| [**Atualizar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Faz com que o controle redesenhe.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Define o interesse do controle InkEdit em um conjunto conhecido de gestos.<br/> |



 



| Propriedade                                                 | Descrição                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aparência**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtém ou define um valor que determina se o controle InkEdit parece simples ou 3D.<br/>                                                                                      |
| [**Fundo**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtém ou define a cor do plano de fundo do controle InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtém ou define um valor que determina se o controle InkEdit tem uma borda.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtém ou define um valor que determina se as barras de rolagem no controle InkEdit estão desabilitadas.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtém ou define os atributos de desenho para tinta que ainda deve ser desenhada no controle InkEdit.<br/>                                                                                |
| [**habilitado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtém ou define um valor que determina se o controle InkEdit pode responder a eventos gerados pelo usuário.<br/>                                                                     |
| [**Facto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtém ou define a constante de [factor](factoid-constants.md) que um objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usa para restringir sua pesquisa para o resultado de reconhecimento.<br/> |
| [**Fonte**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtém ou define a fonte do texto que o controle InkEdit exibe.<br/>                                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtém o identificador de janela ao qual o controle [**InkDisp**](inkdisp-class.md) está associado.<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtém ou define um valor que especifica como a tinta é inserida no controle InkEdit, seja como texto ou como tinta.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtém ou define um valor que especifica se a coleta de tinta está desabilitada, se a tinta é coletada ou se a tinta e os gestos são coletados.<br/>                                               |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtém ou define um valor que especifica se o controle InkEdit é somente leitura ou não.<br/>                                                                                       |
| [**Determinado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtém ou define um valor que indica se um controle InkEdit pode conter um número máximo de caracteres e, em caso afirmativo, especifica o número máximo de caracteres.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtém ou define o ícone de mouse personalizado atual.<br/>                                                                                                                                |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do controle InkEdit.<br/>                                |
| [**Tiverem**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtém ou define um valor que indica se este é um controle de InkEdit multilinha.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtém ou define o período de tempo, em milissegundos, entre o último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado e o início do reconhecimento de texto.<br/>        |
| [**Reconhecedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtém ou define o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) a ser usado para reconhecimento.<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtém ou define o tipo de barras de rolagem que aparecem no controle InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtém ou define o alinhamento a ser aplicado à seleção atual ou ao ponto de inserção (somente tempo de execução).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle InkEdit é negrito (somente tempo de execução).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtém ou define se o texto no controle InkEdit aparecerá na linha de base, como um sobrescrito ou como um subscrito (somente tempo de execução).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtém ou define a cor do texto da seleção de texto atual ou do ponto de inserção (somente tempo de execução).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtém ou define o nome da fonte do texto selecionado dentro do controle InkEdit (somente tempo de execução).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtém ou define o tamanho da fonte do texto selecionado dentro do controle InkEdit (somente tempo de execução).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtém ou define a matriz de objetos [**InkDisp**](inkdisp-class.md) inseridos (se exibidos como tinta) que a seleção atual contém.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtém ou define um valor que permite alternar a aparência da seleção entre a tinta e o texto.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle InkEdit é itálico (somente em tempo de execução).<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtém ou define o número de caracteres selecionados no controle InkEdit (somente tempo de execução).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtém ou define o texto formatado no formato RTF (Rich Text Format) selecionado no controle InkEdit (somente tempo de execução).<br/>                                                          |
| [**InícioDaSeleção**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtém ou define o ponto inicial do texto selecionado na caixa de texto (somente tempo de execução).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtém ou define o texto selecionado dentro do controle InkEdit (somente tempo de execução).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle InkEdit é sublinhado (somente tempo de execução).<br/>                            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtém um valor que especifica se o controle InkEdit está ocioso, coletando tinta ou reconhecendo a tinta (somente tempo de execução).<br/>                                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtém ou define o texto atual na caixa de texto.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtém ou define o texto do controle InkEdit, incluindo todos os códigos RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtém ou define um valor que indica se o mouse pode ser usado como um dispositivo de entrada.<br/>                                                                                      |



 



| Estrutura                                                                    | Descrição                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_STROKEINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contém informações sobre um evento de [**traço**](inkedit-stroke.md) (somente Win32).<br/> |
| [**\_GESTUREINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contém informações sobre um gesto específico (somente Win32).<br/>                       |
| [**\_RECOGNITIONRESULTINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contém informações sobre um resultado de reconhecimento (somente Win32).<br/>                     |



 

## <a name="com-implementation"></a>Implementação COM

Esse objeto implementa a interface com do **IInkEdit** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Referência de controle InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

