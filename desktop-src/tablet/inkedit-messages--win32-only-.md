---
description: O controle InkEdit é uma super classe do controle RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Mensagens InkEdit (somente Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b403e950ca67523620baab6f90a8fef9a47bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296873"
---
# <a name="inkedit-messages-win32-only"></a>Mensagens InkEdit (somente Win32)

O controle [InkEdit](inkedit-control-reference.md) é uma super classe do controle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Cada mensagem **RichEdit** é passada, diretamente na maioria dos casos, e tem exatamente o mesmo efeito que no **RichEdit**. Isso também se aplica a mensagens de notificação de eventos.

Para enviar essas mensagens, chame a função SendMessage com os seguintes parâmetros:



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>LRESULT SendMessage(
  HWND hWnd,      // handle to destination window
  UINT Msg,       // message
  WPARAM wParam,  // first message parameter
  LPARAM lParam   // second message parameter
);</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="message"></a>Mensagem

A janela pai do controle [InkEdit](inkedit-control-reference.md) recebe mensagens de notificação de eventos por meio da mensagem do WM \_ Notify:


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
| em \_ GETINKMODE<br/>           | Obtém o modo de tinta do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores que são definidos na enumeração [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , que especifica se a coleta de tinta está desabilitada, se a tinta é coletada ou se a tinta e os gestos são coletados.<br/>                                                                                                                                                                                                                                                         |
| em \_ SETINKMODE<br/>           | Define o modo de tinta do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Especifica um dos valores da enumeração [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , que especifica se a coleta de tinta está desabilitada, se a tinta é coletada ou se a tinta e os gestos são coletados.<br/>*lParam* Esse parâmetro não é usado; Ele deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/>                                                                                                               |
| em \_ GETINKINSERTMODE<br/>     | Obtém o modo de inserção de tinta do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , que especifica se a tinta é inserida no controle como texto ou como tinta.<br/>                                                                                                                                                                                                                                                                                                    |
| em \_ SETINKINSERTMODE<br/>     | Define o modo de inserção de tinta do controle [InkEdit](inkedit-control-reference.md) . O envio desta mensagem não terá nenhum efeito se for usado com qualquer sistema operacional instalado além do Microsoft Windows XP Tablet PC Edition.<br/> Parâmetros:<br/>*wParam* Especifica um dos valores da enumeração [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , que especifica se a tinta é inserida no controle como texto ou como tinta.<br/>*lParam* Esse parâmetro não é usado; Ele deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                       |
| em \_ GETDRAWATTR<br/>          | Obtém os atributos de desenho atuais do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro (IInkDrawingAttributes \* \* pDrawAttr) para receber o objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                |
| em \_ SETDRAWATTR<br/>          | Define os atributos de desenho a serem usados para a coleta de tinta futura.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro (IInkDrawingAttributes \* pDrawAttr) para um objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                  |
| em \_ GETRECOTIMEOUT<br/>       | Obtém o tempo limite de reconhecimento, em milissegundos, para o controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna o tempo limite de reconhecimento, em milissegundos.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| em \_ SETRECOTIMEOUT<br/>       | Define o tempo limite de reconhecimento, em milissegundos, para o controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Especifica o tempo limite de reconhecimento, em milissegundos.<br/>*lParam* Esse parâmetro não é usado; Ele deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                    |
| em \_ GETGESTURESTATUS<br/>     | Obtém o status do gesto para o controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Especifica o tipo de gesto, conforme definido na enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Esse parâmetro não é usado; Ele deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará **true** se o controle [InkEdit](inkedit-control-reference.md) assinar o gesto ou **false** se o controle InkEdit não assinar o gesto.<br/>                                                                                                                                                                       |
| em \_ SETGESTURESTATUS<br/>     | Define o status do gesto para o controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Especifica o tipo de gesto, conforme definido na enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Especifica **true** se a assinatura do gesto estiver habilitada ou **false** se a escuta do gesto não estiver habilitada.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/>                                                                                                               |
| em \_ GETcognizer<br/>        | Obtém o reconhecedor usado pelo controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para um IInkRecognizer \* para receber o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usado pelo controle [InkEdit](inkedit-control-reference.md) .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                   |
| em \_ Recognizer<br/>        | Define o reconhecedor usado pelo controle [InkEdit](inkedit-control-reference.md) . Se um [factor](factoid-constants.md) for usado para o controle InkEdit, ele deverá ser reaplicado após o envio dessa mensagem.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para um IInkRecognizer \* para definir o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que o controle [InkEdit](inkedit-control-reference.md) usa para uso posterior.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/> |
| em \_ GETfactoid<br/>           | Obtém o [factor](factoid-constants.md) a ser usado para reconhecimento.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para um BSTR para receber a cadeia de caracteres do factor.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| em \_ SETfactoid<br/>           | Define o [factor](factoid-constants.md) a ser usado para reconhecimento.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica o BSTR que contém a cadeia de caracteres do factor.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| em \_ GETSELINK<br/>            | Obtém a tinta dentro da seleção. A tinta deve ser reconhecida antes de ser acessada por essa mensagem. Se não for reconhecido primeiro, em \_ GETSELINK sempre retornará nenhum objeto [**InkDisp**](inkdisp-class.md) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para uma variante para receber uma matriz segura para receber objetos [**InkDisp**](inkdisp-class.md) dentro da seleção atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                     |
| em \_ SETSELINK<br/>            | Define a tinta dentro da seleção. O envio desta mensagem não terá nenhum efeito se for usado com qualquer sistema operacional instalado além do Windows XP Tablet PC Edition.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um ponteiro para uma variante com uma matriz segura de objetos [**InkDisp**](inkdisp-class.md) para substituir a seleção atual.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                     |
| em \_ GETSELINKDISPLAYMODE<br/> | Retorna a aparência atual da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (texto de IDM \_ ou tinta de IDM \_ ), que especifica como uma seleção aparece no controle.<br/>                                                                                                                                                                                                                           |
| em \_ SETSELINKDISPLAYMODE<br/> | Define a aparência da tinta no intervalo selecionado usando um dos valores da enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica como a tinta aparece no intervalo selecionado, conforme definido na enumeração [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro. O envio desta mensagem não terá nenhum efeito se for usado com qualquer sistema operacional instalado além do Windows XP Tablet PC Edition.<br/>                                                                                                   |
| em \_ GETstatus<br/>            | Obtém o status do controle [InkEdit](inkedit-control-reference.md) .<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retorna um dos valores da enumeração [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) , que especifica se o controle está ocioso, coletando tinta ou reconhecendo a tinta.<br/>                                                                                                                                                                                                                                                                                                           |
| \_Recognize<br/>            | Força o reconhecimento.<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| em \_ GETMOUSEICON<br/>         | Obtém o ícone do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Especifica um \* ponteiro HICON que é preenchido com o HICON [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) atual. Esse HICON pode ser um valor de HICON ou **nulo** .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                                                                    |
| em \_ SETMOUSEICON<br/>         | Define o ícone do mouse.<br/> Parâmetros:<br/>*wParam* Especifica um valor BOOLIANo definido como **true** se o controle [InkEdit](inkedit-control-reference.md) deve possuir o identificador HICON ou **false** se o controle INKEDIT não deve possuir o identificador hIcon. Se o controle InkEdit possuir o HICON, ele cuidará e destruirá o HICON adequadamente. Caso contrário, o chamador possui o HICON e é responsável por excluí-lo.<br/>*lParam* Especifica o novo valor HICON. Use **NULL** para limpar o valor. O valor padrão é **NULL**.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                |
| em \_ GETmousepointer<br/>      | Obtém o ponteiro do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Contém um \* ponteiro InkMousePointer que é preenchido com o valor [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) atual. Isso se comporta da mesma forma que a propriedade **InkCollector:: get \_ MousePointer** .<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                                            |
| em \_ SETmousepointer<br/>      | Define o ponteiro do mouse.<br/> Parâmetros:<br/>*wParam* Esse parâmetro não é usado; Ele deve ser 0.<br/>*lParam* Contém o novo valor [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) , que é definido na enumeração [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) . Isso se comporta da mesma forma que o **InkCollector::p UT \_ MousePointer** propriedade.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/>                                                                                                                                                                                                                                    |
| em \_ GETUSEMOUSEFORINPUT<br/>  | Obtém o estado de se a entrada do mouse é tratada como entrada de caneta.<br/> Parâmetros:<br/> Esta mensagem não tem parâmetros; *wParam* e *lParam* devem ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se **for false** ou 1 se **for true**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| em \_ SETUSEMOUSEFORINPUT<br/>  | Define o estado de se a entrada do mouse é tratada como entrada à caneta.<br/> Parâmetros:<br/>*wParam* Especifica um valor booliano que determina se a entrada do mouse deve ser tratada como entrada de caneta.<br/>*lParam* Esse parâmetro não é usado; Ele deve ser 0.<br/> Valores de retorno:<br/> Essa mensagem retornará 0 se for bem-sucedida ou diferente de zero se ocorrer um erro.<br/> Comentários:<br/> Isso só deve ser usado se o em \_ GetStatus retornar s \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Mensagem de notificação de eventos         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IECN \_ traço<br/>            | Notifica a janela pai do controle [InkEdit](inkedit-control-reference.md) que um [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) foi criado. Isso é enviado em uma \_ mensagem de notificação do WM com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura de [**\_ STROKEINFO do IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) .<br/> Valores de retorno:<br/> O cliente retorna 0 para aceitar o traço e 1 para cancelar o traço.<br/> |
| gesto de IECN \_<br/>           | Notifica a janela pai do controle [InkEdit](inkedit-control-reference.md) que um gesto foi reconhecido. Isso é enviado em uma \_ mensagem de notificação do WM com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura de [**\_ GESTUREINFO do IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) .<br/> Valores de retorno:<br/> O cliente retorna 0 para aceitar o gesto e 1 para cancelar o gesto.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Notifica a janela pai do controle [InkEdit](inkedit-control-reference.md) que o reconhecimento ocorreu. Isso é enviado em uma \_ mensagem de notificação do WM com os parâmetros a seguir.<br/> Parâmetros:<br/>*wParam* Especifica o identificador do controle que enviou a mensagem.<br/>*lParam* Especifica um ponteiro para a estrutura de [**\_ RECOGNITIONRESULTINFO do IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) .<br/> Valores de retorno:<br/> O cliente retornará 0 se processar a mensagem.<br/>                                  |



 

## <a name="applies-to"></a>Aplica-se A

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_Estrutura GESTUREINFO IEC (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**\_Estrutura STROKEINFO IEC (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**\_Estrutura RECOGNITIONRESULTINFO IEC (somente Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**Propriedade MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**Enumeração InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**Enumeração InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**Enumeração InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interface IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

