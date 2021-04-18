---
description: Esta seção contém propriedades que pertencem ao controle InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Propriedades de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747684"
---
# <a name="inkedit-properties"></a>Propriedades de InkEdit

Esta seção contém propriedades que pertencem ao controle InkEdit.



| Propriedade                                                 | Descrição                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aparência**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtém ou define um valor que determina se o controle [InkEdit](inkedit-control-reference.md) parece simples ou 3D.<br/>                                                                      |
| [**Fundo**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtém ou define a cor do plano de fundo do controle [InkEdit](inkedit-control-reference.md) .<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtém ou define um valor que determina se o controle [InkEdit](inkedit-control-reference.md) tem uma borda.<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtém ou define um valor que determina se as barras de rolagem no controle [InkEdit](inkedit-control-reference.md) estão desabilitadas.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtém ou define os atributos de desenho para tinta que ainda deve ser desenhada no controle [InkEdit](inkedit-control-reference.md) .<br/>                                                                |
| [**habilitado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtém ou define um valor que determina se o controle [InkEdit](inkedit-control-reference.md) pode responder a eventos gerados pelo usuário.<br/>                                                     |
| [**Facto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtém ou define a constante de [factor](factoid-constants.md) que um objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usa para restringir sua pesquisa para o resultado de reconhecimento.<br/>                  |
| [**Fonte**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtém ou define a fonte do texto que o controle [InkEdit](inkedit-control-reference.md) exibe.<br/>                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtém o identificador de janela ao qual o controle [**InkDisp**](inkdisp-class.md) está associado.<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtém ou define um valor que especifica como a tinta é inserida no controle [InkEdit](inkedit-control-reference.md) , seja como texto ou como tinta.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtém ou define um valor que especifica se a coleta de tinta está desabilitada, se a tinta é coletada ou se a tinta e os gestos são coletados.<br/>                                                                |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtém ou define um valor que especifica se o controle [InkEdit](inkedit-control-reference.md) é somente leitura ou não.<br/>                                                                       |
| [**Determinado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtém ou define um valor que indica se um controle [InkEdit](inkedit-control-reference.md) pode conter um número máximo de caracteres e, em caso afirmativo, especifica o número máximo de caracteres.<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtém ou define o ícone de mouse personalizado atual.<br/>                                                                                                                                                 |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do controle [InkEdit](inkedit-control-reference.md) .<br/>                |
| [**Tiverem**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtém ou define um valor que indica se este é um controle de [InkEdit](inkedit-control-reference.md) multilinha.<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtém ou define o período de tempo, em milissegundos, entre o último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado e o início do reconhecimento de texto.<br/>                         |
| [**Reconhecedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtém ou define o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) a ser usado para reconhecimento.<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtém ou define o tipo de barras de rolagem que aparecem no controle [InkEdit](inkedit-control-reference.md) .<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtém ou define o alinhamento a ser aplicado à seleção atual ou ao ponto de inserção (somente tempo de execução).<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle [InkEdit](inkedit-control-reference.md) é negrito (somente tempo de execução).<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtém ou define se o texto no controle [InkEdit](inkedit-control-reference.md) aparecerá na linha de base, como um sobrescrito ou como um subscrito (somente tempo de execução).<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtém ou define a cor do texto da seleção de texto atual ou do ponto de inserção (somente tempo de execução).<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtém ou define o nome da fonte do texto selecionado dentro do controle [InkEdit](inkedit-control-reference.md) (somente tempo de execução).<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtém ou define o tamanho da fonte do texto selecionado dentro do controle [InkEdit](inkedit-control-reference.md) (somente tempo de execução).<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtém ou define a matriz de objetos [**InkDisp**](inkdisp-class.md) inseridos (se exibidos como tinta) que a seleção atual contém.<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtém ou define um valor que permite alternar a aparência da seleção entre a tinta e o texto.<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle [InkEdit](inkedit-control-reference.md) é itálico (somente em tempo de execução).<br/>                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtém ou define o número de caracteres selecionados no controle [InkEdit](inkedit-control-reference.md) (somente tempo de execução).<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtém ou define o texto formatado no formato RTF (Rich Text Format) selecionado no controle [InkEdit](inkedit-control-reference.md) (somente tempo de execução).<br/>                                          |
| [**InícioDaSeleção**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtém ou define o ponto inicial do texto selecionado na caixa de texto (somente tempo de execução).<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtém ou define o texto selecionado dentro do controle [InkEdit](inkedit-control-reference.md) (somente tempo de execução).<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtém ou define um valor que especifica se o estilo da fonte do texto selecionado no momento no controle [InkEdit](inkedit-control-reference.md) é sublinhado (somente tempo de execução).<br/>            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtém um valor que especifica se o controle [InkEdit](inkedit-control-reference.md) está ocioso, coletando tinta ou reconhecendo a tinta (somente tempo de execução).<br/>                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtém ou define o texto atual na caixa de texto.<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtém ou define o texto do controle [InkEdit](inkedit-control-reference.md) , incluindo todos os códigos RTF.<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtém ou define um valor que indica se o mouse pode ser usado como um dispositivo de entrada.<br/>                                                                                                       |



 

 

 




