---
description: O objeto PenInputPanel permite que você adicione facilmente entrada de caneta in-loco aos seus aplicativos.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Classe PenInputPanel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 58d27b97bb6683f32c145b92c1fda65fe0a786d5cb502e644580b57366119840
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708336"
---
# <a name="peninputpanel-class"></a>Classe PenInputPanel

\[Preterido. **PenInputPanel** foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).\]

O objeto **PenInputPanel** permite que você adicione facilmente entrada de caneta in-loco aos seus aplicativos.

O objeto **PenInputPanel** está disponível como um objeto anexável que permite adicionar funcionalidade do painel de entrada do Tablet PC a controles existentes. A interface do usuário é amplamente exigida pelo idioma de entrada atual. Você tem a opção de escolher o método de entrada padrão para o objeto **PenInputPanel** , um manuscrito ou um teclado. O usuário final pode alternar entre os métodos de entrada usando os botões na interface do usuário.

**PenInputPanel** tem estes tipos de membros:

-   [Enumerações](#enumerations)
-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="enumerations"></a>Enumerações

A classe **PenInputPanel** tem essas enumerações.



| Enumeração                    | Descrição                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Define o tipo de entrada disponível no momento no objeto **PenInputPanel** .<br/> |



 

### <a name="events"></a>Eventos

A classe **PenInputPanel** tem esses eventos.



| Evento                                                  | Descrição                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Ocorre quando o foco de entrada é alterado antes que o objeto **PenInputPanel** pudesse inserir a entrada do usuário no controle anexado.<br/> |
| [**Painelchanged**](peninputpanel-panelchanged.md)     | Ocorre quando o objeto **PenInputPanel** é alterado entre layouts.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Ocorre quando o objeto **PenInputPanel** está sendo movido.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Ocorre quando o objeto **PenInputPanel** é exibido ou oculto.<br/>                                                         |



 

### <a name="interfaces"></a>Interfaces

A classe **PenInputPanel** define essas interfaces.



| Interface          | Descrição                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Esse objeto implementa a interface com do **IPenInputPanel** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **PenInputPanel** tem esses métodos.



| Método                                                         | Descrição                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Envia a tinta coletada para o reconhecedor e posta o resultado do reconhecimento.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Quando passado como **true**, o **PenInputPanel** tenta enviar texto ao controle anexado por meio da estrutura de serviços de texto (TSF) e habilita o uso da interface do usuário de correção.<br/>    |
| [**Mover**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Define a posição do objeto **PenInputPanel** como uma posição de tela estática.<br/>                                                                                                               |
| [**Atualizar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Atualiza e restaura as propriedades **PenInputPanel** com base nas configurações do painel de entrada do Tablet PC, posiciona automaticamente o painel de entrada da caneta e define a interface do usuário para o painel padrão.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **PenInputPanel** tem essas propriedades.



| Propriedade                                                                  | Tipo de acesso           | Descrição                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Leitura/gravação<br/> | Obtém ou define o identificador de janela do controle ao qual o objeto **PenInputPanel** está anexado.<br/>                                                                     |
| [**Mostrar automostrações**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Leitura/gravação<br/> | Obtém ou define um valor booliano que especifica se o objeto **PenInputPanel** aparece quando o foco é definido usando a caneta.<br/>                                           |
| [**Carregado**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Somente leitura<br/>  | Obtém um valor booliano que especifica se o objeto **PenInputPanel** está processando a tinta no momento.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Leitura/gravação<br/> | Obtém ou define qual tipo de painel está sendo usado no momento para entrada dentro do objeto **PenInputPanel** .<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Leitura/gravação<br/> | Obtém ou define qual tipo de painel é o tipo de painel padrão usado para entrada dentro do objeto **PenInputPanel** .<br/>                                                         |
| [**Facto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Leitura/gravação<br/> | Obtém ou define o nome da cadeia de caracteres do factor usado no reconhecimento.<br/>                                                                                                    |
| [**Altura**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Somente leitura<br/>  | Obtém a altura do objeto **PenInputPanel** nas coordenadas do cliente.<br/>                                                                                              |
| [**As**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Leitura/gravação<br/> | Obtém ou define o deslocamento entre a borda esquerda do objeto **PenInputPanel** e a borda esquerda do controle ao qual ele está anexado.<br/>                             |
| [**Mantida**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Somente leitura<br/>  | Obtém o local horizontal, ou eixo x, da borda esquerda do objeto **PenInputPanel** , em coordenadas da tela.<br/>                                                   |
| [**Início**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Somente leitura<br/>  | Obtém o local vertical, ou eixo y, da borda superior do objeto **PenInputPanel** , em coordenadas da tela.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Leitura/gravação<br/> | Obtém ou define o deslocamento entre a borda horizontal mais próxima do objeto **PenInputPanel** e a borda horizontal mais próxima do controle ao qual ele está anexado.<br/> |
| [**Visível**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Leitura/gravação<br/> | Obtém ou define um valor que indica se o objeto **PenInputPanel** está visível.<br/>                                                                                |
| [**Largura**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Somente leitura<br/>  | Obtém a largura do objeto **PenInputPanel** nas coordenadas do cliente.<br/>                                                                                               |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Programando o painel de entrada usando a classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
