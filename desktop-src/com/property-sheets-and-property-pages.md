---
title: Folhas de propriedades e páginas de propriedade
description: Folhas de propriedades e páginas de propriedade
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cc61d1e1ed0cb833632b6b627a0c683a3cb0e4
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103837539"
---
# <a name="property-sheets-and-property-pages"></a>Folhas de propriedades e páginas de propriedade

As propriedades de um objeto são expostas aos clientes da mesma forma que os métodos por meio de interfaces COM ou a implementação **IDispatch** do objeto, permitindo que as propriedades sejam alteradas por programas que chamam esses métodos. A tecnologia OLE das páginas de propriedades fornece os meios para criar uma interface do usuário para as propriedades de um objeto de acordo com os padrões de interface do usuário do Windows. Portanto, as propriedades são expostas aos usuários finais. A folha de propriedades de um objeto é uma caixa de diálogo com guias, onde cada guia corresponde a uma página de propriedades específica. O modelo OLE para trabalhar com páginas de propriedades consiste nesses recursos:

-   Cada página de propriedades é gerenciada por um objeto em processo que implementa [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) ou [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2). Cada página é identificada com seu próprio CLSID exclusivo.
-   Um objeto especifica seu suporte para páginas de propriedades implementando [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Por meio dessa interface, o chamador pode obter uma lista de CLSIDs que identificam as páginas de propriedades específicas às quais o objeto dá suporte. Se o objeto especificar um CLSID de página de propriedades, o objeto deverá ser capaz de receber alterações de propriedade da página de propriedades.
-   Qualquer parte do código (cliente ou objeto) que deseja exibir a folha de propriedades de um objeto passa o ponteiro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto (ou uma matriz se vários objetos devem ser afetados) junto com uma matriz de CLSIDs de página para [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) ou [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), que cria a caixa de diálogo com guias.
-   A caixa de diálogo quadro de propriedades instancia uma única instância de cada página de propriedades, usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em cada CLSID. O quadro de propriedade obtém pelo menos um ponteiro [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) para cada página. Além disso, o quadro cria um objeto de site de página de propriedades em si para cada página. Cada site implementa [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) e esse ponteiro é passado para cada página. Em seguida, a página se comunica com o site por meio desse ponteiro de interface.
-   Cada página também está ciente do objeto ou dos objetos para os quais foi invocado; ou seja, o quadro de propriedades passa os ponteiros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)dos objetos para cada página. Quando instruído a aplicar alterações aos objetos, cada página consulta o ponteiro de interface apropriado e passa novos valores de propriedade para os objetos da maneira desejada. Não há estipulações sobre como essa comunicação deve acontecer.
-   Um objeto também pode dar suporte à navegação por Propriedade por meio da interface [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) , permitindo que o objeto especifique qual propriedade deve receber o foco inicial quando a página de propriedades é exibida e para especificar cadeias de caracteres e valores que podem ser exibidos pelo cliente em sua própria interface do usuário.

Esses recursos são ilustrados no diagrama a seguir:

![Diagrama que mostra as folhas de propriedades e os recursos de páginas de propriedades.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Essas interfaces são definidas da seguinte maneira:

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

O método [**ISpecifyPropertyPages:: GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) retorna uma matriz contada de valores UUID (GUID), cada qual descreve o CLSID de uma página de propriedades que o objeto gostaria de exibir. Quem invoca a folha de propriedades com [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) ou [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) passa essa matriz para a função. Observe que, se o chamador quiser exibir páginas de propriedades para vários objetos, ele só deverá passar a interseção das listas de CLSID de todos os objetos para essas funções. Em outras palavras, o chamador deve invocar apenas as páginas de propriedades que são comuns a todos os objetos.

Além disso, o chamador passa os ponteiros [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) para os objetos afetados para as funções de API também. Ambas as funções de API criam uma caixa de diálogo de quadro de propriedades e instanciam um site de página com [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) para cada página que será carregada. Por meio dessa interface, uma página de propriedades pode:

-   Recupere o idioma atual usado na folha de propriedades por meio de [**Getlocaleid**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Peça ao quadro para processar pressionamentos de tecla por meio de [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Notifique o quadro de alterações na página por meio de [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Obtenha um ponteiro de interface para o quadro em si por meio de [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), embora não haja interfaces definidas para o quadro no momento para essa função sempre retornar E \_ NOTIMPL.

O quadro de propriedades instancia cada objeto de página de propriedades e obtém a interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) de cada página. Por meio dessa interface, o quadro informa a página de seu site de página ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), recupera as dimensões e as cadeias de caracteres de página ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), passa os ponteiros de interface para os objetos afetados ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), informa à página quando criar e destruir seus controles ([**Ativar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) e [**desativar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)), instrui a página a ser mostrada ou reposicionada ([**Mostrar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) e [**mover**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), instrui a página a aplicar seus valores atuais aos objetos afetados ([**aplicar**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), verifica o status sujo da página ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), invoca ajuda ([**ajuda**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) e passa os pressionamentos de teclas para a página ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Um objeto também pode oferecer suporte à navegação por propriedade, que fornece:

1.  Uma maneira (por meio de [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) e [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) para especificar qual propriedade em qual página de propriedades deve receber o foco inicial quando uma folha de propriedades é exibida pela primeira vez
2.  Uma maneira (por meio de [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) para o objeto especificar valores predefinidos e cadeias de caracteres descritivas correspondentes que podem ser exibidos na própria interface do usuário do cliente para propriedades.

Um objeto pode optar por oferecer suporte (2) sem suporte (1), como quando o objeto não tem nenhuma folha de propriedades.

As interfaces [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) e [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) são definidas da seguinte maneira:

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Para especificar seu suporte para esses recursos, o objeto implementa [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). Por meio dessa interface, o chamador pode solicitar as informações necessárias para obter a navegação, como cadeias de caracteres predefinidas ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) e valores ([**getpré-definidosvalue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), bem como uma cadeia de caracteres de exibição para uma determinada propriedade ([**getdisplaystring**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Além disso, o cliente pode obter o CLSID da página de propriedades que permite ao usuário editar uma determinada propriedade identificada com um DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Em seguida, o cliente instrui o quadro de propriedades a ativar essa página inicialmente, passando o CLSID e o DISPID para [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). O quadro ativa essa página primeiro e passa o DISPID para a página por meio de [**IPropertyPage2:: EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). Em seguida, a página define o foco para o campo de edição dessa propriedade. Dessa forma, um cliente pode saltar de um nome de propriedade em sua própria interface de usuário para a página de propriedades que pode manipular essa propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




