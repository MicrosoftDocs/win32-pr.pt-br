---
description: Exibindo páginas de propriedades de um filtro
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Exibindo páginas de propriedades de um filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370073"
---
# <a name="displaying-a-filters-property-pages"></a>Exibindo páginas de propriedades de um filtro

Uma página de propriedades é uma maneira de um filtro oferecer suporte a propriedades que o usuário pode definir. Este artigo descreve como exibir as páginas de propriedades de um filtro em um aplicativo. Para obter mais informações sobre páginas de propriedades, consulte a documentação do Platform SDK.

> [!Note]  
> Embora muitos dos filtros fornecidos com as páginas de propriedades de suporte do DirectShow, eles destinam-se a fins de depuração e não são recomendados para uso do aplicativo. Na maioria dos casos, a funcionalidade equivalente é fornecida por meio de uma interface personalizada no filtro. Um aplicativo deve controlar esses filtros programaticamente, em vez de expor suas páginas de propriedades aos usuários.

 

Filtros com páginas de propriedades expõem a interface **ISpecifyPropertyPages** . Para determinar se um filtro define uma página de propriedades, consulte o filtro para essa interface usando **QueryInterface**.

Se você criou diretamente uma instância de um filtro (chamando **CoCreateInstance**), você já tem um ponteiro para o filtro. Caso contrário, você pode enumerar os filtros no grafo, usando o método [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) . Para obter detalhes, consulte [Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md).

Quando você tiver o ponteiro de interface **ISpecifyPropertyPages** , recupere as páginas de propriedades do filtro chamando o método **ISpecifyPropertyPages:: GetPages** . Esse método preenche uma matriz contada de identificadores globalmente exclusivos (GUIDs) com o identificador de classe (CLSID) de cada página de propriedades. Uma matriz contada é definida por uma estrutura **CAUUID** , que você deve alocar, mas não precisa inicializar. O método **GetPages** aloca a matriz, que está contida no membro **PElems** da estrutura **CAUUID** . Quando terminar, libere a matriz chamando a função **CoTaskMemFree** .

A função **OleCreatePropertyFrame** fornece uma maneira simples de exibir as páginas de propriedades dentro de uma caixa de diálogo modal.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



