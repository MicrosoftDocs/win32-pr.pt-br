---
description: Representa um objeto que é útil para cenários de anotação em que os usuários não se preocupam com a execução de reconhecimento na tinta, mas em vez disso estão interessados no tamanho, na forma, na cor e na posição da tinta.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: Classe InkOverlay (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d1a818c1fef9006abad2dd31da5a41f43aeb3df9a9b75d348d8987938abfcea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967115"
---
# <a name="inkoverlay-class"></a>Classe InkOverlay

Representa um objeto que é útil para cenários de anotação em que os usuários não se preocupam com a execução de reconhecimento na tinta, mas em vez disso estão interessados no tamanho, na forma, na cor e na posição da tinta.

A criação do controle **InkOverlay** por trás de um controle transparente (como uma caixa de grupo com o conjunto de propriedades de WS \_ ex \_ Transparent) impedirá que **InkOverlay** colete a tinta.

**InkOverlay** tem estes tipos de membros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

A classe **InkOverlay** tem esses eventos.



| Evento                                                     | Descrição                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Ocorre quando **InkOverlay** detecta um botão de cursor que está inoperante.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Ocorre quando **InkOverlay** detecta um botão de cursor que está ativo.<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | Ocorre quando a dica de cursor entra na superfície do Tablet de digitalização.<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do Tablet.<br/>                                                                                                                                                  |
| [**Duplo**](inkcollector-doubleclick.md)           | Ocorre quando o objeto **InkOverlay** é clicado duas vezes.<br/>                                                                                                                                                                                       |
| [**Gesto**](inkcollector-gesture.md)                   | Ocorre quando um gesto específico do aplicativo é reconhecido.<br/>                                                                                                                                                                                     |
| [**MouseDown**](inkcollector-mousedown.md)               | Ocorre quando o ponteiro do mouse está sobre o objeto **InkOverlay** e um botão do mouse é pressionado.<br/>                                                                                                                                                 |
| [**Ocorra**](inkcollector-mousemove.md)               | Ocorre quando o ponteiro do mouse é movido sobre o objeto **InkOverlay** .<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | Ocorre quando o ponteiro do mouse está sobre o objeto **InkOverlay** e um botão do mouse é liberado.<br/>                                                                                                                                                |
| [**MouseWheel**](inkcollector-mousewheel.md)             | Ocorre quando a roda do mouse se move enquanto o objeto **InkOverlay** tem foco.<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Ocorre quando um pacote no ar é visto, o que acontece quando um usuário move uma caneta perto do Tablet e o cursor está dentro da janela do objeto **InkOverlay** ou o usuário move um mouse na janela associada do objeto de objeto **InkOverlay** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Ocorre quando o objeto **InkOverlay** recebe pacotes.<br/>                                                                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                     | Ocorre quando o objeto **InkOverlay** conclui o redesenho próprio.<br/>                                                                                                                                                                          |
| [**Pintura**](inkoverlay-painting.md)                   | Ocorre antes que o objeto **InkOverlay** seja redesenhado.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Ocorre quando a seleção de tinta dentro do controle é alterada, como por meio de alterações para a interface do usuário, procedimentos de recortar e colar ou a propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | Ocorre quando a seleção de tinta dentro do controle está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | Ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                      |
| [**Pincel**](inkcollector-stroke.md)                     | Ocorre quando o usuário termina de desenhar um novo traço em qualquer mesa digitalizadora.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Ocorre após os traços serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Ocorre antes de os traços serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Ocorre quando um gesto do sistema é reconhecido.<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é adicionado ao sistema.<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Ocorre quando um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Interfaces

A classe **InkOverlay** define essas interfaces.



| Interface       | Descrição                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Esse objeto implementa a interface com do **IInkOverlay** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkOverlay** tem esses métodos.



| Método                                                                              | Descrição                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Define um retângulo no qual redesenhar a tinta dentro do objeto **InkOverlay** .<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Retorna o estado atual de um evento de objeto **InkOverlay** específico, ou seja, se o evento está sendo escutado ou usado.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Retorna se o objeto **InkOverlay** está interessado em um gesto específico.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera o retângulo da janela, em pixels, no qual a tinta é desenhada.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Determina qual parte da seleção foi atingida durante um teste de clique.<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Esse modo permite que o objeto **InkOverlay** colete tinta de qualquer Tablet anexado ao Tablet PC.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Define se um evento específico deve ser escutado ou usado.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Define o interesse do objeto **InkOverlay** em um gesto conhecido.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Esse modo permite que o objeto **InkOverlay** colete tinta de apenas um Tablet. A tinta de outros tablets é ignorada pelo objeto **InkOverlay** .<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Define o retângulo da janela, em pixels, a ser usado para mapear tinta desenhada para a janela.<br/>                                                                    |



 

### <a name="properties"></a>Propriedades

A classe **InkOverlay** tem essas propriedades.



| Propriedade                                                                                       | Tipo de acesso           | Descrição                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Leitura/gravação<br/> | Obtém ou define o valor que especifica se o objeto **InkOverlay** é anexado atrás ou na frente da janela conhecida.<br/>                                                       |
| [**Redesenhar novamente**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Leitura/gravação<br/> | Obtém ou define um valor que especifica se **InkOverlay** redesenha a tinta quando a janela é invalidada.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Somente leitura<br/>  | Obtém um valor que especifica se a tinta está sendo desenhada no momento em um objeto **InkOverlay** .<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Leitura/gravação<br/> | Obtém ou define o modo de coleta que determina se a tinta, os gestos ou ambos são reconhecidos conforme o usuário escreve.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Somente leitura<br/>  | Obtém a coleção de [**cursores**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponível para uso na região de tinta.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Leitura/gravação<br/> | Obtém ou define o objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) padrão, que especifica os atributos de desenho que são usados ao desenhar e exibir a tinta.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Leitura/gravação<br/> | Obtém ou define o interesse em aspectos do pacote associado à tinta desenhada no objeto **InkOverlay** .<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Leitura/gravação<br/> | Obtém ou define um valor que indica se a tinta é renderizada conforme é desenhada.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Leitura/gravação<br/> | Obtém ou define um valor que indica se **InkOverlay** está no modo de tinta, no modo de exclusão ou no modo de seleção/edição.<br/>                                                          |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Leitura/gravação<br/> | Obtém ou define um valor que especifica se o objeto **InkOverlay** coleta a entrada da caneta.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Leitura/gravação<br/> | Obtém ou define um valor que indica se a tinta é apagada por traço ou por ponto.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Leitura/gravação<br/> | Obtém ou define um valor que especifica a largura da dica de caneta do apagador.<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Leitura/gravação<br/> | Obtém ou define o identificador da janela à qual o objeto **InkOverlay** está anexado.<br/>                                                                                             |
| [**Tinta**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Leitura/gravação<br/> | Obtém ou define o objeto [**InkDisp**](inkdisp-class.md) associado ao objeto **InkOverlay** .<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Leitura/gravação<br/> | Obtém ou define as margens ao longo do eixo x, em pixels.<br/>                                                                                                                             |
| [**Margem**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Leitura/gravação<br/> | Obtém ou define as margens ao longo do eixo y, em pixels.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Leitura/gravação<br/> | Obtém ou define o ícone de mouse personalizado atual.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Leitura/gravação<br/> | Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do objeto.<br/>                                                |
| [**Renderizador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Leitura/gravação<br/> | Obtém ou define o objeto [**InkRenderer**](inkrenderer-class.md) usado para desenhar tinta.<br/>                                                                                        |
| [**Seleção**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Leitura/gravação<br/> | Obtém ou define a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada no momento dentro do controle **InkOverlay** .<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Leitura/gravação<br/> | Obtém ou define um valor que especifica se a tinta é renderizada como apenas uma cor quando o sistema está no modo de Alto Contraste.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Leitura/gravação<br/> | Obtém ou define um valor que especifica se toda a interface do usuário de seleção é desenhada em alto contraste quando o sistema está no modo de Alto Contraste.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Somente leitura<br/>  | Obtém o dispositivo do Tablet que o objeto **InkOverlay** está usando no momento para coletar a entrada.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Notas de implementação do MFC

Se você anexou o objeto InkOverlay a um objeto Cvisualização, libere o objeto InkOverlay em resposta à mensagem de destruição do WM, \_ conforme mostrado no exemplo a seguir:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

O objeto **InkOverlay** é adequado para observações e scribbling básicas. O uso pretendido principal deste objeto é exibir a tinta como tinta.

Em geral, a interface do usuário de tempo de execução para esse objeto é uma janela transparente com tinta opaca.

Os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)e [**MouseWheel**](inkcollector-mousewheel.md) retornam as coordenadas x e y em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esses eventos substituem os eventos de mouse de aplicativos sem reconhecimento de caneta e esses aplicativos entendem apenas pixels.

> [!Caution]  
> Se você estiver definindo a propriedade [**anexámode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) do objeto **InkOverlay** como Infront, crie o objeto **InkOverlay** no thread em que o formulário está em execução. Seu aplicativo pode parar de responder se o objeto **InkOverlay** for criado em um thread diferente e sua propriedade **AttachMode** estiver definida como Infront.

 

> [!Note]  
> O objeto **InkOverlay** não pode ser liberado com segurança em um thread que não seja de interface do usuário.

 

Para melhorar o desempenho do aplicativo, descarte o objeto **InkOverlay** quando ele não for mais necessário.

Se você anexou o objeto InkOverlay a um objeto Cvisualização, libere o objeto InkOverlay em resposta à mensagem de destruição do WM, \_ conforme mostrado no exemplo a seguir:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[Referência de controle InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Referência de controle InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

