---
title: Como criar uma folha de propriedades
description: O exemplo nesta seção cria uma folha de propriedades que contém duas páginas \ 8212; uma para definir as propriedades de fonte de uma célula em uma planilha e outra para definir as propriedades de borda da célula.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa99c3e678fa7d8e6aa70cd3f5c6e4c7bc514f94114c7bb7a411fa7df1caac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831842"
---
# <a name="how-to-create-a-property-sheet"></a>Como criar uma folha de propriedades

O exemplo nesta seção cria uma folha de propriedades que contém duas páginas — uma para definir as propriedades de fonte de uma célula em uma planilha e outra para definir as propriedades de borda da célula.

O exemplo define as páginas preenchendo um par de estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) e especificando o endereço na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) que é passado para a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="create-a-property-sheet"></a>Criar uma folha de propriedades

O exemplo de código a seguir demonstra como criar uma folha de propriedades de duas páginas.


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a>Comentários

Os modelos, ícones e rótulos da caixa de diálogo para as páginas são carregados dos recursos contidos no arquivo executável do aplicativo. O ícone da folha de propriedades também é carregado dos recursos do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando folhas de propriedades](using-property-sheets.md)
</dt> <dt>

[Exemplo de propriedade](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




