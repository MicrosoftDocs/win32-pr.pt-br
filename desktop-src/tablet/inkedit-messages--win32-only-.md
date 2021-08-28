---
description: O controle InkEdit é uma super classe do controle RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Mensagens InkEdit (somente Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475032"
---
# <a name="inkedit-messages-win32-only"></a>Mensagens InkEdit (somente Win32)

O [controle InkEdit](inkedit-control-reference.md) é uma super classe do [**controle RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) Cada **mensagem RichEdit** é passada, diretamente na maioria dos casos, e tem exatamente o mesmo efeito que no **RichEdit.** Isso também se aplica a mensagens de notificação de eventos.

Para enviar essas mensagens, chame a função SendMessage com os seguintes parâmetros:




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>Mensagem

A janela pai do controle [InkEdit](inkedit-control-reference.md) recebe mensagens de notificação de eventos por meio da mensagem WM \_ NOTIFY:


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Obter/definir mensagem                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ GETINKMODE<br/>           | Obtém o modo de tinta do [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/> Essa mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores definidos na enumeração [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) que especifica se a coleção de tinta está desabilitada, se a tinta é coletada ou se tinta e gestos são coletados.<br/>                                                                                                                                                                                                                                                         |
| EM \_ SETINKMODE<br/>           | Define o modo de tinta do [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/>*wParam* Especifica um dos valores da enumeração [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) que especifica se a coleção de tinta está desabilitada, se a tinta é coletada ou se a tinta e os gestos são coletados.<br/>*lParam* Esse parâmetro não é usado; deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deverá ser usado se o EM \_ GETSTATUS retornar IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETINKINERTMODE<br/>     | Obtém o modo de inserção de tinta do [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/> Essa mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) que especifica se a tinta é inserida no controle como texto ou como tinta.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETINKINERTMODE<br/>     | Define o modo de inserção de tinta do [controle InkEdit.](inkedit-control-reference.md) O envio dessa mensagem não terá efeito se for usado com qualquer sistema operacional instalado que não seja o Microsoft Windows XP Tablet PC Edition.<br/> Parâmetros:<br/>*wParam* Especifica um dos valores da enumeração [**InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) que especifica se a tinta é inserida no controle como texto ou como tinta.<br/>*lParam* Esse parâmetro não é usado; deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/>                                                                                                       |
| EM \_ GETDRAWATTR<br/>          | Obtém os atributos de desenho atuais do [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; deve ser 0.<br/>*lParam* Especifica um ponteiro (IInkDrawingAttributes \* \* pDrawAttr) para receber o objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                |
| EM \_ SETDRAWATTR<br/>          | Define os atributos de desenho a usar para a coleção de tinta futura.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; deve ser 0.<br/>*lParam* Especifica um ponteiro (IInkDrawingAttributes \* pDrawAttr) para [**um objeto InkDrawingAttributes.**](inkdrawingattributes-class.md)<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ GETRECOTIMEOUT<br/>       | Obtém o tempo de tempo de reconhecimento, em milissegundos, para o [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/> Essa mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna o tempo de tempo de reconhecimento, em milissegundos.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ SETRECOTIMEOUT<br/>       | Define o tempo de tempo de reconhecimento, em milissegundos, para o [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/>*wParam* Especifica o tempo de tempo de reconhecimento, em milissegundos.<br/>*lParam* Esse parâmetro não é usado; deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GETGESTURESTATUS<br/>     | Obtém o status do gesto para o [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/>*wParam* Especifica o tipo de gesto, conforme definido na [**enumeração InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Esse parâmetro não é usado; deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem **retornará TRUE** se o [controle InkEdit](inkedit-control-reference.md) assinar o gesto ou **FALSE** se o controle InkEdit não assinar o gesto.<br/>                                                                                                                                                                       |
| EM \_ SETGESTURESTATUS<br/>     | Define o status do gesto para o [controle InkEdit.](inkedit-control-reference.md)<br/> Parâmetros:<br/>*wParam* Especifica o tipo de gesto, conforme definido na [**enumeração InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Especifica **TRUE se** a assinatura do gesto está habilitada ou **FALSE** se a escuta do gesto não está habilitada.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deverá ser usado se o EM \_ GETSTATUS retornar IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETRECOGNIZER<br/>        | Obtém o reconhecedor que o [controle InkEdit](inkedit-control-reference.md) usa.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; deve ser 0.<br/>*lParam* Especifica um ponteiro para um IInkRecognizer para receber o objeto \* [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que o [controle InkEdit](inkedit-control-reference.md) usa.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                   |
| EM \_ SETRECOGNIZER<br/>        | Define o reconhecedor que o [controle InkEdit](inkedit-control-reference.md) usa. Se um [Factoid](factoid-constants.md) for usado para o controle InkEdit, ele deverá ser reaplicado depois de enviar essa mensagem.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; deve ser 0.<br/>*lParam* Especifica um ponteiro para um IInkRecognizer para definir o objeto \* [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que o [controle InkEdit](inkedit-control-reference.md) usa para uso posterior.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/> |
| em \_ GETfactoid<br/>           | Obtém o [factor](factoid-constants.md) a ser usado para reconhecimento.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para um BSTR para receber a cadeia de caracteres do factor.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| em \_ SETfactoid<br/>           | Define o [factor](factoid-constants.md) a ser usado para reconhecimento.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica o BSTR que contém a cadeia de caracteres do factor.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| em \_ GETSELINK<br/>            | Obtém a tinta dentro da seleção. A tinta deve ser reconhecida antes de ser acessada por essa mensagem. Se não for reconhecido primeiro, em \_ GETSELINK sempre retornará nenhum objeto [**InkDisp**](inkdisp-class.md) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para uma variante para receber uma matriz segura para receber objetos [**InkDisp**](inkdisp-class.md) dentro da seleção atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                     |
| em \_ SETSELINK<br/>            | Define a tinta dentro da seleção. o envio desta mensagem não terá nenhum efeito se for usado com qualquer sistema operacional instalado além do Windows XP Tablet PC Edition.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para uma variante com uma matriz segura de objetos [**InkDisp**](inkdisp-class.md) para substituir a seleção atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                     |
| em \_ GETSELINKDISPLAYMODE<br/> | Retorna a aparência atual da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (texto de IDM \_ ou tinta de IDM \_ ), que especifica como uma seleção aparece no controle.<br/>                                                                                                                                                                                                                           |
| em \_ SETSELINKDISPLAYMODE<br/> | Define a aparência da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica como a tinta aparece no intervalo selecionado, conforme definido na enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro. o envio desta mensagem não terá nenhum efeito se for usado com qualquer sistema operacional instalado além do Windows XP Tablet PC Edition.<br/>                                                                                                   |
| em \_ GETstatus<br/>            | Obtém o status do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) , que especifica se o controle está ocioso, coletando tinta ou reconhecendo a tinta.<br/>                                                                                                                                                                                                                                                                                                           |
| \_Recognize<br/>            | Força o reconhecimento.<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| em \_ GETMOUSEICON<br/>         | Obtém o ícone do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um \* ponteiro HICON que é preenchido com o HICON [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) atual. Esse HICON pode ser um valor de HICON ou **nulo** .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                    |
| em \_ SETMOUSEICON<br/>         | Define o ícone do mouse.<br/> Parâmetros:<br/>*wParam* Especifica um valor BOOLIANo definido como **true** se o controle [InkEdit](inkedit-control-reference.md) deve possuir o identificador HICON ou **false** se o controle INKEDIT não deve possuir o identificador hIcon. Se o controle InkEdit possuir o HICON, ele cuidará e destruirá o HICON adequadamente. Caso contrário, o chamador possui o HICON e é responsável por excluí-lo.<br/>*lParam* Especifica o novo valor HICON. Use **NULL** para limpar o valor. O valor padrão é **NULL**.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                |
| em \_ GETmousepointer<br/>      | Obtém o ponteiro do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Contém um \* ponteiro InkMousePointer que é preenchido com o valor [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) atual. Isso se comporta da mesma forma que a propriedade **InkCollector:: get \_ MousePointer** .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                            |
| em \_ SETmousepointer<br/>      | Define o ponteiro do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Contém o novo valor [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) , que é definido na enumeração [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) . Isso se comporta da mesma forma que o **InkCollector::p UT \_ MousePointer** propriedade.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                    |
| em \_ GETUSEMOUSEFORINPUT<br/>  | Obtém o estado de se a entrada do mouse é tratada como entrada de caneta.<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se **FALSE** ou 1 se **TRUE.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETUSEMOUSEFORINPUT<br/>  | Define o estado de se a entrada do mouse é tratada como entrada de caneta.<br/> Parâmetros:<br/>*wParam* Especifica um valor booliana que determina se a entrada do mouse deve ser tratado como entrada de caneta.<br/>*lParam* Esse parâmetro não é usado; deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou não zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deverá ser usado se o EM \_ GETSTATUS retornar IES \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Mensagem de notificação de evento         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRAÇO \_ IECN<br/>            | Notifica a janela pai do controle [InkEdit](inkedit-control-reference.md) de que [**um IInkRogkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) foi criado. Isso é enviado em uma mensagem WM \_ NOTIFY com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura [**\_ STROKEINFO do IEC.**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)<br/> Valores de retorno:<br/> O cliente retorna 0 para aceitar o traço e 1 para cancelar o traço.<br/> |
| GESTO \_ IECN<br/>           | Notifica a janela [pai do controle InkEdit](inkedit-control-reference.md) de que um gesto foi reconhecido. Isso é enviado em uma mensagem WM \_ NOTIFY com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura [**\_ IEC GESTUREINFO.**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)<br/> Valores de retorno:<br/> O cliente retorna 0 para aceitar o gesto e 1 para cancelar o gesto.<br/>                           |
| RECONHECIMENTO DE \_ IECNRESULT<br/> | Notifica a janela [pai do controle InkEdit](inkedit-control-reference.md) de que o reconhecimento ocorreu. Isso é enviado em uma mensagem WM \_ NOTIFY com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura [**IEC \_ RECOGNITIONRESULTINFO.**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)<br/> Valores de retorno:<br/> O cliente retornará 0 se ele processa a mensagem.<br/>                                  |



 

## <a name="applies-to"></a>Aplica-se A

-   [Inkedit](inkedit-control-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Estrutura IEC \_ GESTUREINFO (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**Estrutura STROKEINFO do IEC \_ (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**Estrutura IEC \_ RECOGNITIONRESULTINFO (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**Propriedade MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**Enumeração InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**Enumeração InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**Enumeração InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkRecognitionResult Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**IInkRecognizer Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**IInkGesture Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

