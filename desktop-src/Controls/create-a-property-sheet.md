---
title: Como criar uma folha de propriedades
description: O exemplo nesta seção cria uma folha de propriedades que contém duas páginas \ 8212; uma para definir as propriedades de fonte de uma célula em uma planilha e outra para definir as propriedades de borda da célula.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105748100"
---
# <a name="how-to-create-a-property-sheet"></a><span data-ttu-id="1fe6b-103">Como criar uma folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="1fe6b-103">How to Create a Property Sheet</span></span>

<span data-ttu-id="1fe6b-104">O exemplo nesta seção cria uma folha de propriedades que contém duas páginas — uma para definir as propriedades de fonte de uma célula em uma planilha e outra para definir as propriedades de borda da célula.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-104">The example in this section creates a property sheet that contains two pages—one for setting the font properties of a cell in a spreadsheet, and another for setting the border properties of the cell.</span></span>

<span data-ttu-id="1fe6b-105">O exemplo define as páginas preenchendo um par de estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) e especificando o endereço na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) que é passado para a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .</span><span class="sxs-lookup"><span data-stu-id="1fe6b-105">The example defines the pages by filling a pair of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures and specifying the address in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that is passed to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1fe6b-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="1fe6b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1fe6b-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="1fe6b-107">Technologies</span></span>

-   [<span data-ttu-id="1fe6b-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="1fe6b-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1fe6b-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1fe6b-109">Prerequisites</span></span>

-   <span data-ttu-id="1fe6b-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="1fe6b-110">C/C++</span></span>
-   <span data-ttu-id="1fe6b-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="1fe6b-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1fe6b-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="1fe6b-112">Instructions</span></span>

### <a name="create-a-property-sheet"></a><span data-ttu-id="1fe6b-113">Criar uma folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="1fe6b-113">Create a Property Sheet</span></span>

<span data-ttu-id="1fe6b-114">O exemplo de código a seguir demonstra como criar uma folha de propriedades de duas páginas.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-114">The following code example demonstrates how to create a two–page property sheet.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="1fe6b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fe6b-115">Remarks</span></span>

<span data-ttu-id="1fe6b-116">Os modelos, ícones e rótulos da caixa de diálogo para as páginas são carregados dos recursos contidos no arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-116">The dialog box templates, icons, and labels for the pages are loaded from the resources contained in the application's executable file.</span></span> <span data-ttu-id="1fe6b-117">O ícone da folha de propriedades também é carregado dos recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-117">The icon for the property sheet is also loaded from the application's resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fe6b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fe6b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fe6b-119">Usando folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="1fe6b-119">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

[<span data-ttu-id="1fe6b-120">Exemplo de propriedade</span><span class="sxs-lookup"><span data-stu-id="1fe6b-120">Property sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




