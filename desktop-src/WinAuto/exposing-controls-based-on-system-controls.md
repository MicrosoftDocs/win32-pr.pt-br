---
title: Expondo controles com base em controles do sistema
description: Expondo controles com base em controles do sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366476"
---
# <a name="exposing-controls-based-on-system-controls"></a>Expondo controles com base em controles do sistema

Você deve considerar o uso de alguma forma de anotação dinâmica — direta, mapa de valor ou servidor — antes de tentar a técnica descrita nesta seção. Para obter mais informações, consulte [API de anotação dinâmica](dynamic-annotation-api.md).

Na maioria dos casos, a Microsoft Acessibilidade Ativa expõe informações sobre os controles de subclasse ou de subclasse. A superclasse e a subclasse permitem que um desenvolvedor de aplicativo crie um controle personalizado com a funcionalidade básica de um controle do sistema e inclua aprimoramentos fornecidos pelo aplicativo. Um controle superclasse tem um nome de classe de janela diferente do controle do sistema no qual ele se baseia. Um controle de subclasse tem o mesmo nome de classe de janela. Para obter mais informações sobre a superclasse e a subclasse, consulte a documentação do SDK (Software Development Kit) do Windows.

Como a Microsoft Acessibilidade Ativa expõe informações sobre controles fornecidos pelo sistema, a Microsoft Acessibilidade Ativa expõe o controle modificado, a menos que um controle de subclasse ou de subclasse seja significativamente diferente do controle base. Para determinar se o controle modificado está acessível, os desenvolvedores de aplicativos devem usar utilitários como [inspecionar](inspect-objects.md) e [Inspetor de eventos acessível](accessible-event-watcher.md) para comparar o comportamento do controle modificado com o controle de base.

Se, depois de usar esses utilitários, você determinar que o controle modificado não está acessível, você deve tratar o controle como qualquer outro controle personalizado. O controle deve disparar eventos, e o procedimento de janela do aplicativo deve responder à mensagem do [**WM \_ GetObject**](wm-getobject.md)fornecendo uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que os aplicativos cliente usam para obter informações sobre o controle.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy e CreateStdAccessibleObject

Se todas ou a maior parte das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do controle modificado forem as mesmas do controle base, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) ou [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) para simplificar a implementação da interface **IAccessible** do controle.

> [!Note]  
> Ao superclasse ou subclasse de um controle acessível, lembre-se de que o objeto recuperado pela função [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pode implementar mais do que apenas a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Ele pode incluir outras interfaces, como [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant). Talvez seja necessário encapsular essas interfaces adicionais para manter o suporte de acessibilidade fornecido pelo implementação original do controle.

 

As funções [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) e [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperam um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o controle do sistema especificado. A diferença nessas funções é que **CreateStdAccessibleObject** usa o nome de classe da janela obtido de seu parâmetro *HWND* , enquanto **CreateStdAccessibleProxy** usa o nome de classe da janela especificado em seu parâmetro *szClassName* . Portanto, se você decidir usar essas funções, use **CreateStdAccessibleProxy** para expor informações sobre controles superclasses e qualquer função com controles de subclasse.

Depois de obter um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o controle do sistema, use o ponteiro em sua implementação da interface **IAccessible** para o controle modificado. Se uma propriedade ou método para o controle modificado for o mesmo que o controle base, use o ponteiro **IAccessible** para retornar as informações fornecidas pelo controle de base. Se uma propriedade para o controle modificado for diferente do controle base, substitua a propriedade do controle base.

No exemplo a seguir, **CAccCustomButton** é a classe definida pelo aplicativo derivada de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). A variável de membro **m \_ pAccDefaultButton** é um ponteiro para uma interface **IAccessible** que foi recuperada de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante o procedimento de inicialização do controle. Neste exemplo, a propriedade **role** do controle personalizado é igual à propriedade **role** do controle do sistema, portanto, a propriedade **role** do controle base é retornada. No entanto, a propriedade **Description** é diferente da do controle base, portanto, essa propriedade é substituída.


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



Para obter mais informações sobre as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e métodos de controles do sistema, consulte [o apêndice A: referência de elementos da interface do usuário com suporte](appendix-a--supported-user-interface-elements-reference.md).

 

 