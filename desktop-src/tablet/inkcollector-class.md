---
description: Representa o objeto usado para capturar tinta de dispositivos tablet disponíveis.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Classe InkCollector (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718172"
---
# <a name="inkcollector-class"></a>Classe InkCollector

Representa o objeto usado para capturar tinta de dispositivos tablet disponíveis.

A criação **do controle InkCollector** por trás de um controle transparente (como uma GroupBox com o conjunto de **propriedades \_ WS EX \_ TRANSPARENT)** impedirá que **o InkCollector** colete tinta.

**InkCollector** tem estes tipos de membros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

A **classe InkCollector** tem esses eventos.



| Evento                                                     | Descrição                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Ocorre quando o **InkCollector** detecta um botão de cursor que está inocos.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Ocorre quando o **InkCollector** detecta um botão de cursor que está para cima.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Ocorre quando a dica de cursor contata a superfície de tablet de digitalização.<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do tablet.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do tablet.<br/>                                                                                                                                                      |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Ocorre quando o **objeto InkCollector** é clicado duas vezes.<br/>                                                                                                                                                                                         |
| [**Gesto**](inkcollector-gesture.md)                   | Ocorre quando um gesto específico do aplicativo é reconhecido.<br/>                                                                                                                                                                                         |
| [**Mousedown**](inkcollector-mousedown.md)               | Ocorre quando o ponteiro do mouse está sobre o **objeto InkCollector** e um botão do mouse é pressionado.<br/>                                                                                                                                                   |
| [**Mousemove**](inkcollector-mousemove.md)               | Ocorre quando o ponteiro do mouse é movido sobre o **objeto InkCollector.**<br/>                                                                                                                                                                           |
| [**Mouseup**](inkcollector-mouseup.md)                   | Ocorre quando o ponteiro do mouse está sobre o **objeto InkCollector** e um botão do mouse é liberado.<br/>                                                                                                                                                  |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Ocorre quando a roda do mouse se move enquanto o **objeto InkCollector** tem foco.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Ocorre quando um in-air packet é visto, o que acontece quando um usuário move uma caneta perto do tablet e o cursor está dentro da janela do objeto **InkCollector** ou o usuário move um mouse dentro da janela associada do objeto **InkCollector.**<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Ocorre quando o **objeto InkCollector** recebe pacotes.<br/>                                                                                                                                                                                          |
| [**Curso**](inkcollector-stroke.md)                     | Ocorre quando o usuário termina de desenhar um novo traço em qualquer tablet.<br/>                                                                                                                                                                                  |
| [**Systemgesture**](inkcollector-systemgesture.md)       | Ocorre quando um gesto do sistema é reconhecido.<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Ocorre quando um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é adicionado ao sistema.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Ocorre quando um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfaces

A **classe InkCollector** define essas interfaces.



| Interface         | Descrição                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Esse objeto implementa a interface **COM IInkCollector.**<br/> |



 

### <a name="methods"></a>Métodos

A **classe InkCollector** tem esses métodos.



| Método                                                                              | Descrição                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Recupera o estado atual de um evento **de objeto InkCollector** específico, ou seja, se o evento está sendo ouvido ou usado.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Recupera se o **objeto InkCollector** está interessado em um gesto específico.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera o retângulo da janela, em pixels, dentro do qual a tinta é desenhada.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Esse modo permite que o **objeto InkCollector** colete tinta de qualquer tablet anexado ao tablet.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifica um valor que indica se um evento específico deve ser ouvido ou usado.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifica o interesse do objeto **InkCollector** em um gesto conhecido.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Esse modo permite que o **objeto InkCollector** colete tinta de apenas um tablet. A tinta de outros tablets é ignorada pelo **objeto InkCollector.**<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifica o retângulo da janela, em pixels, a ser usado para mapear a tinta desenhada para a janela.<br/>                                                                    |



 

### <a name="properties"></a>Propriedades

A **classe InkCollector** tem essas propriedades.



| Propriedade                                                                             | Tipo de acesso          | Descrição                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Somente leitura<br/> | Obtém ou define um valor que especifica se **o InkCollector** reintsifique a tinta quando a janela é invalidada.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Somente leitura<br/> | Obtém um valor que especifica se a tinta está sendo desenhada no momento em um **objeto InkCollector.**<br/>                                                                                   |
| [**Collectionmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Somente leitura<br/> | Obtém ou define o modo de coleta que determina se tinta, gestos ou ambos são reconhecidos como gravações do usuário.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Somente leitura<br/> | Obtém [**a coleção Cursores**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponível para uso na região de inking.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Somente leitura<br/> | Obtém ou define o [**objeto InkDrawingAttributes**](inkdrawingattributes-class.md) padrão, que especifica os atributos de desenho usados ao desenhar e exibir tinta.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Somente leitura<br/> | Obtém ou define o interesse nos aspectos do pacote associado à tinta desenhada no **objeto InkCollector.**<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Somente leitura<br/> | Obtém ou define um valor que indica se a tinta é renderizada conforme é desenhada.<br/>                                                                                                       |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Somente leitura<br/> | Obtém ou define um valor que especifica se o objeto **InkCollector** coleta a entrada da caneta.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Somente leitura<br/> | Obtém ou define o identificador da janela à qual o objeto **InkCollector** está anexado.<br/>                                                                                           |
| [**Tinta**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Somente leitura<br/> | Obtém ou define o objeto [**InkDisp**](inkdisp-class.md) associado ao objeto **InkCollector** .<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Somente leitura<br/> | Obtém ou define as margens ao longo do eixo x, em pixels.<br/>                                                                                                                             |
| [**Margem**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Somente leitura<br/> | Obtém ou define as margens ao longo do eixo y, em pixels.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Somente leitura<br/> | Obtém ou define o ícone de mouse personalizado atual.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Somente leitura<br/> | Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do objeto.<br/>                                                |
| [**Renderizador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Somente leitura<br/> | Obtém ou define o objeto [**InkRenderer**](inkrenderer-class.md) usado para desenhar tinta.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Somente leitura<br/> | Obtém ou define um valor que especifica se a tinta é renderizada como apenas uma cor quando o sistema está no modo de Alto Contraste.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Somente leitura<br/> | Obtém o dispositivo do Tablet que o objeto **InkCollector** está usando no momento para coletar a entrada.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

O objeto **InkCollector** coleta somente tinta e gestos que são inseridos na janela específica à qual está associado. A única finalidade do **InkCollector** é coletar tinta do hardware (por exemplo, por meio de um objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) ) e fornecê-lo a um aplicativo. Ele essencialmente atua como a origem que distribui a tinta em um ou vários objetos [**InkDisp**](inkdisp-class.md) diferentes, que atuam como contêiner que mantém a tinta distribuída.

Para usar um **InkCollector**, você o cria, informa em qual janela coletar tinta desenhada e habilitá-la. Depois de habilitado, ele pode ser definido para coletar em apenas um dos três modos (o modo é especificado na enumeração [**InkCollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) ):

-   InkOnly, no qual um objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) é criado.
-   GestureOnly, no qual um objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) é criado.
-   InkAndGesture, no qual um traço, um gesto ou potencialmente ambos são criados, dependendo de como o aplicativo manipula eventos.

Isso significa que, para cada movimento de um cursor que esteja dentro do intervalo de um Tablet, o **InkCollector** sempre coleta um gesto ou uma pincel e, às vezes, ambos. O suporte a gestos é criado usando o reconhecedor de gestos da Microsoft.

Um **InkCollector** manipula todas as entradas do Tablet. A tinta pode ser coletada de todos os tablets conectados (incluindo o mouse) simultaneamente. As alterações nos objetos [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) podem fazer com que o objeto **InkCollector** dispare um evento.

Um **InkCollector** também gerencia a lista de cursores que ele encontra durante sua existência. Quando o **InkCollector** encontra um novo cursor, o evento [**CursorInRange**](inkcollector-cursorinrange.md) é acionado com o parâmetro *newCursor* definido como **Variant \_ true**. Os aplicativos usam o **InkCollector** para gerenciar novos cursores.

Mais de um **InkCollector** pode ser associado a um identificador de janela específico, mesmo que suas áreas de coleção, definidas no construtor ou com o método [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) , se sobreponham. No entanto, a única maneira como esse cenário funciona é se cada **InkCollector** chama [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) e usa um Tablet exclusivo. Esse comportamento facilita o armazenamento de tinta em um objeto separado para cada Tablet.

Ocorrerá um erro se o retângulo de entrada da janela de um **InkCollector** habilitado (definido com a propriedade [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) ) sobrepor o retângulo de entrada da janela de outro **InkCollector** habilitado.

> [!Note]  
> A sobreposição pode ocorrer sem erro, contanto que apenas um dos retângulos de entrada esteja habilitado em um momento conhecido.

 

Os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)e [**MouseWheel**](inkcollector-mousewheel.md) retornam coordenadas x e y em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta. Isso ocorre porque esses eventos substituem os eventos de mouse de aplicativos sem reconhecimento de caneta e esses aplicativos entendem apenas pixels.

> [!Note]  
> O objeto **InkCollector** não pode ser liberado com segurança em um thread que não seja da interface do usuário.

 

Para melhorar o desempenho do aplicativo, descarte seu objeto **InkCollector** quando ele não for mais necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de controle InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Referência de controle InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

