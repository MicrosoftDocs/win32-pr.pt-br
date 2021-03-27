---
description: Você pode usar a caixa de diálogo fonte comum para exibir as fontes disponíveis.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Criando uma fonte lógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4398f426ae2dd0f18c21409422dfbcb53f0e6ee8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967689"
---
# <a name="creating-a-logical-font"></a>Criando uma fonte lógica

Você pode usar a caixa de diálogo **fonte** comum para exibir as fontes disponíveis. A caixa de diálogo **ChooseFont** é exibida depois que um aplicativo Inicializa os membros de uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e chama a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . Depois que o usuário seleciona uma das fontes disponíveis e pressiona o botão **OK** , a função **ChooseFont** Inicializa uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) com os dados relevantes. Seu aplicativo pode então chamar a função [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) e criar uma fonte lógica com base na solicitação do usuário. O exemplo a seguir demonstra como isso é feito.


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
