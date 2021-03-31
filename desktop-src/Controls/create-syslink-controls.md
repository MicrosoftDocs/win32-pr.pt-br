---
title: Como criar controles SysLink
description: Você implementa os hiperlinks do controle SysLink por meio de marcação na cadeia de caracteres de inicialização do controle ou enviando a ele uma \_ mensagem SETITEM do LM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641938"
---
# <a name="how-to-create-syslink-controls"></a>Como criar controles SysLink

Você implementa os hiperlinks do controle SysLink por meio de marcação na cadeia de caracteres de inicialização do controle ou enviando a ele uma mensagem [**\_ SETITEM do LM**](lm-setitem.md) .

> [!Note]  
> Antes de criar controles SysLink, você deve chamar a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando a \_ classe de link ICC \_ .

 

Para criar um SysLink, chame a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela do [**\_ link WC**](common-control-window-classes.md) . O parâmetro *lpWindowName* que é comum a essas funções especifica um ponteiro para uma cadeia de caracteres terminada em zero que contém o texto marcado para exibição. Para estilos de janela específicos para controles SysLink, consulte [estilos de controle Syslink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

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

Supõe-se que [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) já foi chamado.

A especificação do estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) garante que o usuário poderá selecionar um link alternando-o para ele e pressionando a tecla Enter.

A versão 6 do ComCtl32.dll dá suporte apenas a Unicode. Portanto, você não pode criar versões ANSI de controles SysLink – somente Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 