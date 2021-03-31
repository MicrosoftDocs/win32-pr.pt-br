---
title: Como usar métodos Tab em TOM
description: O exemplo a seguir fornece funções C que ilustram o uso dos métodos Tab no modelo de objeto de texto (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823616"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="5bb24-103">Como usar métodos Tab em TOM</span><span class="sxs-lookup"><span data-stu-id="5bb24-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="5bb24-104">O exemplo a seguir fornece funções C que ilustram o uso dos métodos Tab no modelo de objeto de texto (TOM).</span><span class="sxs-lookup"><span data-stu-id="5bb24-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="5bb24-105">Supõe-se que a maioria dos aplicativos inclui uma barra de ferramentas que mostra a posição atual e o tipo das guias para o parágrafo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="5bb24-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5bb24-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="5bb24-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5bb24-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="5bb24-107">Technologies</span></span>

-   [<span data-ttu-id="5bb24-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="5bb24-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5bb24-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb24-109">Prerequisites</span></span>

-   <span data-ttu-id="5bb24-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="5bb24-110">C/C++</span></span>
-   <span data-ttu-id="5bb24-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="5bb24-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5bb24-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="5bb24-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="5bb24-113">Usar um método de tabulação</span><span class="sxs-lookup"><span data-stu-id="5bb24-113">Use a Tab Method</span></span>

<span data-ttu-id="5bb24-114">O exemplo de código a seguir demonstra como atualizar uma barra de ferramentas com os detalhes da guia atual.</span><span class="sxs-lookup"><span data-stu-id="5bb24-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="5bb24-115">Copiar informações da guia</span><span class="sxs-lookup"><span data-stu-id="5bb24-115">Copy Tab Information</span></span>

<span data-ttu-id="5bb24-116">O exemplo a seguir mostra como copiar apenas as informações da guia de uma interface [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) para outra.</span><span class="sxs-lookup"><span data-stu-id="5bb24-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="5bb24-117">São necessários dois parâmetros: **ITextPara** \* *pParaFrom* (o parágrafo do qual copiar as guias) e **ITextPara** \* *pParaFrom* (o parágrafo para o qual copiar tabulações).</span><span class="sxs-lookup"><span data-stu-id="5bb24-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="5bb24-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bb24-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bb24-119">Usando o modelo de objeto de texto</span><span class="sxs-lookup"><span data-stu-id="5bb24-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="5bb24-120">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="5bb24-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="5bb24-121">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5bb24-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




