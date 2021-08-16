---
description: A classe CBasePropertyPage é uma classe abstrata para implementar uma página de propriedades. Use essa classe se você estiver escrevendo um filtro (ou outro objeto) que dê suporte a páginas de propriedades.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Classe CBasePropertyPage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ca4bf0789488a8601ae24bd4e43e1af8335fdf97a7864cbfba242b9c99eca8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955006"
---
# <a name="cbasepropertypage-class"></a>Classe CBasePropertyPage

![hierarquia de classe CBasePropertyPage](images/cprop01.png)

A `CBasePropertyPage` classe é uma classe abstrata para implementar uma página de propriedades. Use essa classe se você estiver escrevendo um filtro (ou outro objeto) que dê suporte a páginas de propriedades.



| Variáveis de membro protegido                                             | Descrição                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**\_bDirty m**](cbasepropertypage-m-bdirty.md)                        | Indica se alguma das propriedades foi alterada.                                                                             |
| [**\_caixa de diálogo m**](cbasepropertypage-m-dialogid.md)                    | Identificador de recurso da caixa de diálogo.                                                                                               |
| [**m \_ Dlg**](cbasepropertypage-m-dlg.md)                              | Identificador para a janela de diálogo.                                                                                                      |
| [**\_HWND m**](cbasepropertypage-m-hwnd.md)                            | Identificador para a janela de diálogo.                                                                                                      |
| [**\_pPageSite m**](cbasepropertypage-m-ppagesite.md)                  | Ponteiro para a interface **IPropertyPageSite** do site da página de propriedades.                                                         |
| [**\_título m**](cbasepropertypage-m-titleid.md)                      | Identificador de recurso para uma cadeia de caracteres que contém o título da caixa de diálogo.                                                                  |
| Métodos públicos                                                         | Descrição                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | Método de construtor.                                                                                                               |
| [**~ CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | Método destruidor. VirtuaisLUNs.                                                                                                       |
| [**OnActivate**](cbasepropertypage-onactivate.md)                     | Chamado quando a página de propriedades é ativada. VirtuaisLUNs.                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | Chamado quando o usuário aplica alterações à página de propriedades. VirtuaisLUNs.                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | Fornece um ponteiro **IUnknown** para o objeto associado à página de propriedades. VirtuaisLUNs.                                        |
| [**OnActivate**](cbasepropertypage-ondeactivate.md)                 | Chamado quando a janela da caixa de diálogo é destruída. VirtuaisLUNs.                                                                          |
| [**Desconectar**](cbasepropertypage-ondisconnect.md)                 | Chamado quando a página de propriedades deve liberar o objeto associado. VirtuaisLUNs.                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | Chamado quando a caixa de diálogo recebe uma mensagem. VirtuaisLUNs.                                                                           |
| Métodos IPropertyPage                                                  | Descrição                                                                                                                       |
| [**Ativar**](cbasepropertypage-activate.md)                         | Cria a janela da caixa de diálogo.                                                                                                    |
| [**Usar**](cbasepropertypage-apply.md)                               | Aplica os valores da página de propriedades atual ao objeto associado à página de propriedades                                          |
| [**Desativar**](cbasepropertypage-deactivate.md)                     | Destrói a janela da caixa de diálogo.                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | Recupera informações sobre a página de propriedades.                                                                                    |
| [**Ajuda**](cbasepropertypage-help.md)                                 | Chama a ajuda da página de propriedades.                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | Indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para **IPropertyPage:: apply**. |
| [**Mover**](cbasepropertypage-move.md)                                 | Posiciona e redimensiona a caixa de diálogo.                                                                                             |
| [**Objetos**](cbasepropertypage-setobjects.md)                     | Fornece ponteiros **IUnknown** para os objetos associados à página de propriedades.                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | Inicializa a página de propriedades.                                                                                                    |
| [**Mostrar**](cbasepropertypage-show.md)                                 | Mostra ou oculta a caixa de diálogo.                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | Instrui a página de propriedades para processar um pressionamento de tecla.                                                                               |



 

## <a name="remarks"></a>Comentários

Uma página de propriedades é um objeto COM, portanto, você deve gerar um GUID para o identificador de classe (CLSID) e fornecer uma entrada na matriz [**CFactoryTemplate**](cfactorytemplate.md) . para obter mais informações, consulte [DirectShow e COM](directshow-and-com.md). O exemplo a seguir mostra uma entrada de fábrica de classe típica:


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



O filtro deve expor a interface **ISpecifyPropertyPages** . Essa interface contém um único método, **GetPages**, que retorna o CLSID da página de propriedades. O exemplo a seguir mostra como implementar esse método:


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



Lembre-se de substituir o método **NonDelegatingQueryInterface** do filtro também. para obter mais informações, consulte [DirectShow e COM](directshow-and-com.md) e [**INonDelegatingUnknown**](inondelegatingunknown.md).

Em seguida, crie a caixa de diálogo como um recurso em seu projeto e crie um recurso de cadeia de caracteres que contém o título da caixa de diálogo. Ambas as IDs de recurso são parâmetros para o construtor **CBasePropertyPage** . Manter a cadeia de título em um recurso torna mais fácil localizar sua página de propriedades.

A classe **CBasePropertyPage** fornece uma estrutura para a interface **IPropertyPage** . Essa estrutura chama um número de métodos virtuais, incluindo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md)e assim por diante. Na classe base, esses métodos simplesmente retornam S \_ OK. Sua classe derivada precisará substituir alguns ou todos esses métodos virtuais. Para obter detalhes, consulte os comentários para os métodos individuais.

Para obter um exemplo estendido de como usar essa classe para criar uma página de propriedades, consulte [criando uma página de propriedades de filtro](creating-a-filter-property-page.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




