---
title: Como rotular botões da barra de ferramentas dinamicamente
description: Você pode atribuir texto a um botão existente usando a mensagem TB \_ SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104453892"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Como rotular botões da barra de ferramentas dinamicamente

Você pode atribuir texto a um botão existente usando a mensagem [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="dynamically-label-a-toolbar-button"></a>Rotular dinamicamente um botão da barra de ferramentas

O exemplo a seguir demonstra como alterar o texto do terceiro botão nos exemplos anteriores de **salvar** para **salvar como**.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Comentários

Alterar o texto de um botão usando [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) não afeta a cadeia de caracteres atribuída a esse botão na lista de cadeias de caracteres internas.

Se você adicionar uma cadeia de caracteres de botão da barra de ferramentas à lista de texto interna, não será possível recuperar o índice dessa cadeia de caracteres chamando [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md)— você deve usar a mensagem de [**\_ SetButton de TB**](tb-getbutton.md) em vez disso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




