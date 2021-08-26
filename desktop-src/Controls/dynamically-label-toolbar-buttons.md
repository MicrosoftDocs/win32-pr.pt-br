---
title: Como rotular dinamicamente os botões da barra de ferramentas
description: Você pode atribuir texto a um botão existente usando a mensagem TB \_ SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877436"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Como rotular dinamicamente os botões da barra de ferramentas

Você pode atribuir texto a um botão existente usando a [**mensagem TB \_ SETBUTTONINFO.**](tb-setbuttoninfo.md)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="dynamically-label-a-toolbar-button"></a>Rotular dinamicamente um botão de barra de ferramentas

O exemplo a seguir demonstra como alterar o texto do terceiro botão nos exemplos anteriores de **Salvar** para **Salvar como**.


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

Alterar o texto de um botão usando [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) não afeta a cadeia de caracteres atribuída a esse botão na lista de cadeias de caracteres interna.

Se você adicionar uma cadeia de caracteres de botão de barra de ferramentas à lista de texto interna, não poderá recuperar o índice dessa cadeia de caracteres chamando [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)– você deverá usar a mensagem [**\_ GETBUTTON de TB.**](tb-getbutton.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




