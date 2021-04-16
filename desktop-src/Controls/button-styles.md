---
title: Estilos de botão (WinUser. h)
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
ms.openlocfilehash: 2b0054920f3cb2ae323a9655b1b028da473e119f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747706"
---
# <a name="button-styles"></a>Estilos de botão

Especifica uma combinação de estilos de botão. Se você criar um botão usando a classe BUTTON com a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , poderá especificar qualquer um dos estilos de botão listados abaixo.

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
Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) no github.


## <a name="constants"></a>Constantes
| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**\_3STATE BS**</dt> </dl>                            | Cria um botão que é o mesmo que uma caixa de seleção, exceto que a caixa pode ser acinzentada, bem como marcada ou desmarcada. Use o estado acinzentado para mostrar que o estado da caixa de seleção não é determinado.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**\_AUTO3STATE BS**</dt> </dl>                | Cria um botão que é o mesmo que uma caixa de seleção de três Estados, exceto que a caixa altera seu estado quando o usuário a seleciona. O estado percorre a verificação, indeterminado e limpo.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**CAIXA de seleção autobs \_**</dt> </dl>          | Cria um botão que é o mesmo que uma caixa de seleção, exceto que o estado de verificação alterna automaticamente entre marcado e limpo sempre que o usuário marca a caixa de seleção.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**AUTORADIOBUTTON BS \_**</dt> </dl> | Cria um botão que é igual a um botão de opção, exceto que, quando o usuário o seleciona, o sistema define automaticamente o estado de verificação do botão como marcado e define automaticamente o estado de verificação para que todos os outros botões no mesmo grupo sejam limpos.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**\_bitmap BS**</dt> </dl>                            | Especifica que o botão exibe um bitmap. Consulte a seção comentários para sua interação com o \_ ícone de BS.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**\_parte inferior da BS**</dt> </dl>                            | Coloca o texto na parte inferior do retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**centro do BS \_**</dt> </dl>                            | Centraliza o texto horizontalmente no retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**\_caixa de seleção BS**</dt> </dl>                      | Cria uma caixa de seleção pequena e vazia com texto. Por padrão, o texto é exibido à direita da caixa de seleção. Para exibir o texto à esquerda da caixa de seleção, combine esse sinalizador com o estilo BS \_ LEFTTEXT (ou com o estilo equivalente de \_ RIGHTBUTTON do BS).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**\_COMMANDLINK BS**</dt> </dl>             | Cria um botão de link de comando que se comporta como um \_ botão de estilo de pressão de BS, mas o botão de link de comando tem uma seta verde à esquerda apontando para o texto do botão. Uma legenda para o texto do botão pode ser definida enviando a mensagem de conjunto do BCM \_ ao botão.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**\_DEFCOMMANDLINK BS**</dt> </dl>    | Cria um botão de link de comando que se comporta como um \_ botão de estilo de pressão do BS. Se o botão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão de link de comando pressionando a tecla ENTER, mesmo quando o botão de link de comando não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**\_DEFPUSHBUTTON BS**</dt> </dl>       | Cria um botão de ação que se comporta como um botão de estilo de pressão de BS \_ , mas tem uma aparência distinta. Se o botão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão pressionando a tecla ENTER, mesmo quando o botão não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**\_DEFSPLITBUTTON BS**</dt> </dl>    | Cria um botão de divisão que se comporta como um botão de estilo de pressão de BS \_ , mas também tem uma aparência distinta. Se o botão de divisão estiver em uma caixa de diálogo, o usuário poderá selecionar o botão dividir pressionando a tecla ENTER, mesmo quando o botão de divisão não tiver o foco de entrada. Esse estilo é útil para permitir que o usuário selecione rapidamente a opção mais provável (padrão).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**GroupBox da BS \_**</dt> </dl>                      | Cria um retângulo no qual outros controles podem ser agrupados. Qualquer texto associado a esse estilo é exibido no canto superior esquerdo do retângulo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**ícone de BS \_**</dt> </dl>                                  | Especifica que o botão exibe um ícone. Consulte a seção comentários para sua interação com o \_ bitmap BS.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ plano**</dt> </dl>                                  | Especifica que o botão é bidimensional; Ele não usa o sombreamento padrão para criar uma imagem 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**esquerda da BS \_**</dt> </dl>                                  | Justifica o texto no retângulo do botão. No entanto, se o botão for uma caixa de seleção ou um botão de opção que não tenha o \_ estilo BS RIGHTBUTTON, o texto será justificado à esquerda no lado direito da caixa de seleção ou botão de opção.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**\_LEFTTEXT BS**</dt> </dl>                      | Coloca o texto no lado esquerdo do botão de opção ou caixa de seleção quando combinado com um botão de opção ou estilo de caixa de seleção. O mesmo que o \_ estilo de RIGHTBUTTON BS.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**multilinha de BS \_**</dt> </dl>                   | Encapsula o texto do botão em várias linhas se a cadeia de texto for muito longa para caber em uma única linha no retângulo do botão.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**\_notificação BS**</dt> </dl>                            | Habilita um botão para enviar os códigos de notificação [bilhão \_ KILLFOCUS](bn-killfocus.md) e [bilhão \_ SETFOCUS](bn-setfocus.md) para sua janela pai. <br/> Observe que os botões enviam o código de notificação [ \_ clicado bilhão](bn-clicked.md) , independentemente de ele ter esse estilo. Para obter os códigos de notificação [bilhão \_ DBLCLK](bn-dblclk.md) , o botão deve ter o \_ estilo BS RadioButton ou BS \_ OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**\_OWNERDRAW BS**</dt> </dl>                   | Cria um botão de desenho proprietário. A janela do proprietário recebe uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) quando um aspecto visual do botão é alterado. Não combine o estilo BS \_ OWNERDRAW com outros estilos de botão.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**pressão do BS \_**</dt> </dl>                | Cria um botão de ação que posta uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) na janela do proprietário quando o usuário seleciona o botão.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**\_PUSHLIKE BS**</dt> </dl>                      | Faz com que um botão (como uma caixa de seleção, uma caixa de seleção de três Estados ou um botão de opção) pareça e atue como um botão de ação. O botão é gerado quando não é enviado por Push ou verificado, e baixo relevo quando é enviado por Push ou marcado.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**\_botão de opção BS**</dt> </dl>             | Cria um círculo pequeno com texto. Por padrão, o texto é exibido à direita do círculo. Para exibir o texto à esquerda do círculo, combine esse sinalizador com o \_ estilo BS LEFTTEXT (ou com o estilo RIGHTBUTTON de BS equivalente \_ ). Use botões de opção para grupos de opções relacionadas, mas mutuamente exclusivas.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ à direita**</dt> </dl>                               | Justifica o texto no retângulo do botão. No entanto, se o botão for uma caixa de seleção ou um botão de opção que não tenha o \_ estilo BS RIGHTBUTTON, o texto será justificado à direita no lado direito da caixa de seleção ou botão de opção.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**\_RIGHTBUTTON BS**</dt> </dl>             | Posiciona o círculo de um botão de opção ou um quadrado da caixa de seleção no lado direito do retângulo do botão. O mesmo que o \_ estilo de LEFTTEXT BS.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | Cria um botão de divisão. Um botão de divisão tem uma seta suspensa.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**texto de BS \_**</dt> </dl>                                  | Especifica que o botão exibe texto.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**\_parte superior da BS**</dt> </dl>                                     | Coloca o texto na parte superior do retângulo do botão.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**\_TYPEMASK BS**</dt> </dl>                      | Não use este estilo. Um bit de estilo composto que resulta do uso do operador OR em \_ \* bits de estilo BS. Ele pode ser usado para mascarar \_ \* bits de BS válidos de uma determinada bitmask. Observe que isso está desatualizado e não inclui corretamente todos os estilos válidos. Portanto, você não deve usar esse estilo.<br/>                                                                                               |
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



 

