---
title: Estilos de botão (Winuser.h)
description: Especifica uma combinação de estilos de botão. Se você criar um botão usando a classe BUTTON com a função CreateWindow ou CreateWindowEx, poderá especificar qualquer um dos estilos de botão listados abaixo.
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832476"
---
# <a name="button-styles"></a>Estilos de botão

Especifica uma combinação de estilos de botão. Se você criar um botão usando a classe BUTTON com a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) poderá especificar qualquer um dos estilos de botão listados abaixo.

## <a name="example"></a>Exemplo

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
Exemplo de [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) GitHub.


## <a name="constants"></a>Constantes
| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | Cria um botão que é o mesmo que uma caixa de seleção, exceto pelo fato de que a caixa pode ficar es cinza, bem como marcada ou desempurada. Use o estado es cinza para mostrar que o estado da caixa de seleção não é determinado.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | Cria um botão que é o mesmo que uma caixa de seleção de três estados, exceto que a caixa altera seu estado quando o usuário o seleciona. O estado passa pelo verificado, indeterminado e limpo.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**BS \_ AUTOCHECKBOX**</dt> </dl>          | Cria um botão que é o mesmo que uma caixa de seleção, exceto pelo fato de que o estado de verificação alterna automaticamente entre marcado e limpo sempre que o usuário seleciona a caixa de seleção.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**BS \_ AUTORADIOBUTTON**</dt> </dl> | Cria um botão que é o mesmo que um botão de opção, exceto que, quando o usuário o seleciona, o sistema define automaticamente o estado de verificação do botão como marcado e define automaticamente o estado de verificação para todos os outros botões no mesmo grupo a ser limpo.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**BS \_ BITMAP**</dt> </dl>                            | Especifica que o botão exibe um bitmap. Consulte a seção Comentários para sua interação com o ÍCONE \_ BS.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ BOTTOM**</dt> </dl>                            | Coloca o texto na parte inferior do retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**BS \_ CENTER**</dt> </dl>                            | Centraliza o texto horizontalmente no retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**CAIXA DE \_ SELEÇÃO BS**</dt> </dl>                      | Cria uma caixa de seleção pequena e vazia com texto. Por padrão, o texto é exibido à direita da caixa de seleção. Para exibir o texto à esquerda da caixa de seleção, combine esse sinalizador com o estilo LEFTTEXT BS (ou com o estilo \_ EQUIVALENTE BS \_ RIGHTBUTTON).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | Cria um botão de link de comando que se comporta como um botão de estilo BS PUSHBUTTON, mas o botão de link de comando tem uma seta verde à esquerda apontando para o texto \_ do botão. Uma legenda para o texto do botão pode ser definida enviando a mensagem BCM \_ SETNOTE para o botão.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | Cria um botão de link de comando que se comporta como um botão de estilo \_ BS PUSHBUTTON. Se o botão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão de link de comando pressionando a tecla ENTER, mesmo quando o botão de link de comando não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPTONEBUTTON**</dt> </dl>       | Cria um botão de push que se comporta como um botão de estilo BS \_ PUSHBUTTON, mas tem uma aparência distinta. Se o botão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão pressionando a tecla ENTER, mesmo quando o botão não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | Cria um botão de divisão que se comporta como um botão de estilo BS \_ PUSHBUTTON, mas também tem uma aparência distinta. Se o botão de divisão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão de divisão pressionando a tecla ENTER, mesmo quando o botão de divisão não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**BS \_ GROUPBOX**</dt> </dl>                      | Cria um retângulo no qual outros controles podem ser agrupados. Qualquer texto associado a esse estilo é exibido no canto superior esquerdo do retângulo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**ÍCONE \_ BS**</dt> </dl>                                  | Especifica que o botão exibe um ícone. Consulte a seção Comentários para sua interação com o \_ BITMAP BS.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ FLAT**</dt> </dl>                                  | Especifica que o botão é bidimensional; ele não usa o sombreamento padrão para criar uma imagem 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS \_ LEFT**</dt> </dl>                                  | A esquerda justifica o texto no retângulo do botão. No entanto, se o botão for uma caixa de seleção ou um botão de rádio que não tenha o estilo BS RIGHTBUTTON, o texto será deixado justificado no lado direito da caixa de seleção ou botão \_ de rádio.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | Coloca texto no lado esquerdo do botão de rádio ou caixa de seleção quando combinado com um botão de rádio ou estilo de caixa de seleção. O mesmo que o estilo \_ BS RIGHTBUTTON.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ MULTILINE**</dt> </dl>                   | Quebra o texto do botão em várias linhas se a cadeia de caracteres de texto for muito longa para caber em uma única linha no retângulo do botão.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**BS \_ NOTIFY**</dt> </dl>                            | Habilita um botão para enviar códigos de notificação [BN \_ KILLFOCUS](bn-killfocus.md) e [BN \_ SETFOCUS](bn-setfocus.md) para sua janela pai. <br/> Observe que os botões enviam o código de notificação [ \_ BN CLICKED,](bn-clicked.md) independentemente de ele ter esse estilo. Para obter [códigos de notificação \_ BN DBLCLK,](bn-dblclk.md) o botão deve ter o estilo BS \_ RADIOBUTTON ou BS \_ OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OWNERDRAW**</dt> </dl>                   | Cria um botão desenhado pelo proprietário. A janela proprietário recebe uma [**mensagem WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual do botão é alterado. Não combine o estilo BS \_ OWNERDRAW com nenhum outro estilo de botão.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**BS \_ PUSHBUTTON**</dt> </dl>                | Cria um botão de push que posta uma [**mensagem WM \_ COMMAND**](/windows/desktop/menurc/wm-command) na janela do proprietário quando o usuário seleciona o botão.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | Faz com que um botão (como uma caixa de seleção, caixa de seleção de três estados ou botão de rádio) pareça e aja como um botão de push. O botão parece elevado quando ele não é pressionado ou marcado e esquente quando é pressionado ou marcado.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**BS \_ RADIOBUTTON**</dt> </dl>             | Cria um pequeno círculo com texto. Por padrão, o texto é exibido à direita do círculo. Para exibir o texto à esquerda do círculo, combine esse sinalizador com o estilo LEFTTEXT BS (ou com o \_ estilo BS \_ RIGHTBUTTON equivalente). Use botões de opção para grupos de opções relacionadas, mas mutuamente exclusivas.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ RIGHT**</dt> </dl>                               | Justifica com a direita o texto no retângulo do botão. No entanto, se o botão for uma caixa de seleção ou um botão de rádio que não tenha o estilo BS RIGHTBUTTON, o texto será justificado à direita no lado direito da caixa de seleção ou do botão \_ de rádio.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**BS \_ RIGHTBUTTON**</dt> </dl>             | Posiciona o círculo de um botão de rádio ou o quadrado de uma caixa de seleção no lado direito do retângulo do botão. O mesmo que o estilo \_ LEFTTEXT BS.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | Cria um botão de divisão. Um botão de divisão tem uma seta para baixo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**BS \_ TEXT**</dt> </dl>                                  | Especifica que o botão exibe texto.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ TOP**</dt> </dl>                                     | Coloca o texto na parte superior do retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**BS \_ TYPEMASK**</dt> </dl>                      | Não use esse estilo. Um bit de estilo composto que resulta do uso do operador OR em \_ bits de estilo BS. \* Ele pode ser usado para mascarar bits BS \_ \* válidos de um bitmask determinado. Observe que isso está des date e não inclui corretamente todos os estilos válidos. Portanto, você não deve usar esse estilo.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BOTÃO userbs \_**</dt> </dl>                | Obsoleto, mas fornecido para compatibilidade com versões de 16 bits do Windows. Os aplicativos devem usar BS \_ OWNERDRAW em vez disso.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | Coloca o texto no meio (verticalmente) do retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Comentários

Para obter ilustrações dos estilos do botão principal, como a \_ caixa de seleção BS e o BS \_ , consulte [tipos de botão](button-types-and-styles.md).

A aparência do texto ou um ícone ou ambos em um controle de botão depende do ícone de BS \_ e dos \_ estilos de bitmap BS, e se a mensagem [**\_ SetImage BM**](bm-setimage.md) é enviada. Os resultados possíveis são os seguintes.



| \_Ícone de BS ou \_ bitmap BS definido? | BM \_ SetImage chamada? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sim                         | Sim                  | Mostrar apenas o ícone.     |
| Não                          | Sim                  | Mostrar ícone e texto. |
| Sim                         | Não                   | Mostrar somente texto.     |
| Não                          | Não                   | Mostrar somente texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinUser. h</dt> </dl> |



 

