---
title: Como criar controles SysLink
description: Implemente os hiperlinks do controle SysLink por meio da marcação na cadeia de caracteres de inicialização do controle ou enviando uma mensagem \_ LM SETITEM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878506"
---
# <a name="how-to-create-syslink-controls"></a>Como criar controles SysLink

Implemente os hiperlinks do controle SysLink por meio da marcação na cadeia de caracteres de inicialização do controle ou enviando uma mensagem [**\_ LM SETITEM.**](lm-setitem.md)

> [!Note]  
> Antes de criar controles SysLink, você deve chamar a [**função InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) especificando a CLASSE DE LINK do ICC. \_ \_

 

Para criar um SysLink, chame a [**função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando a classe de janela LINK do [**WC. \_**](common-control-window-classes.md) O *parâmetro lpWindowName* que é comum a essas funções especifica um ponteiro para uma cadeia de caracteres terminada em zero que contém o texto marcado para exibição. Para estilos de janela específicos para controles SysLink, consulte [Estilos de controle SysLink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="create-a-syslink-control"></a>Criar um controle SysLink

O código de exemplo a seguir cria um controle SysLink que exibe dois hiperlinks. O primeiro hiperlink é uma URL da Internet e o segundo é definido pelo aplicativo.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Comentários

Supõe-se que [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) já tenha sido chamado.

Especificar o [**estilo \_ TABSTOP**](/windows/desktop/winmsg/window-styles) do WS garante que o usuário seja capaz de selecionar um link tabulando-o e pressionando a tecla Enter.

A versão 6 do ComCtl32.dll dá suporte apenas a Unicode. Portanto, você não pode criar versões ANSI de controles SysLink – somente Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 