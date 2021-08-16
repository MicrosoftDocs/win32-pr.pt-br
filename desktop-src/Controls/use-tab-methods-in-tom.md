---
title: Como usar métodos tab no TOM
description: O exemplo a seguir fornece funções C que ilustram o uso dos métodos tab no TOM (Modelo de Objeto de Texto).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b4a101c2deb3c22993f41b11ee94df6ac738da41963046f02a072f3eaa6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828608"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Como usar métodos tab no TOM

O exemplo a seguir fornece funções C que ilustram o uso dos métodos tab no TOM (Modelo de Objeto de Texto). Supõe-se que a maioria dos aplicativos inclua uma barra de ferramentas que mostra a posição atual e o tipo das guias para o parágrafo selecionado no momento.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-a-tab-method"></a>Usar um método Tab

O exemplo de código a seguir demonstra como atualizar uma barra de ferramentas com os detalhes da guia atual.


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



### <a name="copy-tab-information"></a>Copiar informações da guia

O exemplo a seguir mostra como copiar apenas as informações da guia de uma interface [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) para outra. Ele aceita dois parâmetros: **ITextPara** pParaFrom (o parágrafo do qual copiar guias) e \*  **ITextPara** \* *pParaFrom* (o parágrafo para o qual copiar guias).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modelo de objeto de texto](using-the-text-object-model.md)
</dt> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




