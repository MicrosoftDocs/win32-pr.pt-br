---
title: Adicionando a funcionalidade de automação da interface do usuário a servidores Acessibilidade Ativa
description: Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o IAccessible, podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário, implementando a interface IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automação da interface do usuário, servidores de Acessibilidade Ativa
- Automação da interface do usuário, Microsoft Acessibilidade Ativa Servers
- Automação da interface do usuário, IAccessible
- Automação da interface do usuário, IAccessibleEx
- Automação da interface do usuário, expondo IAccessibleEx
- Automação da interface do usuário, implementando IAccessibleEx
- IAccessible
- IAccessibleEx
- Acessibilidade Ativa da Microsoft
- Acessibilidade Ativa
- expondo IAccessibleEx
- Implementando IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917360"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>Adicionando a funcionalidade de automação da interface do usuário a servidores Acessibilidade Ativa

Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário, implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Essa interface permite que o controle exponha Propriedades de automação da interface do usuário e padrões de controle, sem a necessidade de uma implementação completa das interfaces do provedor de automação da interface do usuário, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para implementar **IAccessibleEx**, a hierarquia de objetos de linha de base do Microsoft acessibilidade ativa não deve conter erros ou inconsistências (como um objeto filho cujo objeto pai não o lista como um filho) e não deve entrar em conflito com as especificações de automação da interface do usuário. Se a hierarquia de objetos do Microsoft Acessibilidade Ativa atender a esses requisitos, será um bom candidato para adicionar funcionalidades usando o **IAccessibleEx**; caso contrário, você deve implementar a automação da interface do usuário sozinha ou junto com a implementação do Microsoft Acessibilidade Ativa.

Use o caso de um controle personalizado que tenha um valor de intervalo. O Microsoft Acessibilidade Ativa Server para o controle define sua função e é capaz de retornar seu valor atual, mas não tem o meio de retornar os valores mínimo e máximo do controle, pois essas propriedades não são definidas no Microsoft Acessibilidade Ativa. Um cliente de automação de interface do usuário é capaz de recuperar a função do controle, o valor atual e outras propriedades do Microsoft Acessibilidade Ativa, porque o núcleo de automação da interface do usuário pode obtê-los por meio do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). No entanto, sem acesso a uma interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) no objeto, a automação da interface do usuário também não consegue recuperar os valores mínimo e máximo.

O desenvolvedor de controle poderia fornecer um provedor de automação de interface do usuário completo para o controle, mas isso significaria duplicar grande parte da funcionalidade existente da implementação do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por exemplo, navegação e propriedades comuns. Em vez disso, o desenvolvedor pode continuar a confiar no **IAccessible** para fornecer essa funcionalidade, ao mesmo tempo em que adiciona suporte para propriedades específicas de controle por meio de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

A atualização do controle personalizado requer estas etapas principais:

-   Implemente [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) no objeto acessível para que a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa ser encontrada neste ou em um objeto separado.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no objeto acessível.
-   Crie objetos distintos acessíveis para qualquer item filho da Microsoft Acessibilidade Ativa, que no Microsoft Acessibilidade Ativa pode ter sido representado pela interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto pai (por exemplo, itens de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nesses objetos.
-   Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) em todos os objetos acessíveis.
-   Implemente as interfaces de padrão de controle apropriadas nos objetos acessíveis.

Este tópico inclui as seções a seguir.

-   [Expondo IAccessibleEx](#exposing-iaccessibleex)
-   [Implementando IAccessibleEx](#implementing-iaccessibleex)
-   [Tópicos relacionados](#related-topics)

## <a name="exposing-iaccessibleex"></a>Expondo IAccessibleEx

Como a implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para um controle pode residir em um objeto separado, os aplicativos cliente não podem confiar em [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter essa interface. Em vez disso, os clientes devem chamar [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)). Na implementação de exemplo a seguir desse método, supõe-se que **IAccessibleEx** não está implementado em um objeto separado; Portanto, o método simplesmente chama para **QueryInterface**.


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>Implementando IAccessibleEx

O método de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) que é da maior parte do seu interesse é [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild). Esse método dá ao Microsoft Acessibilidade Ativa Server uma oportunidade de criar um objeto acessível (um que expõe, no mínimo, **IAccessibleEx**) para um item filho. No Microsoft Acessibilidade Ativa, os itens filho normalmente não são representados como objetos acessíveis, mas como filhos de um objeto acessível. No entanto, como a automação da interface do usuário requer que cada elemento seja representado por um objeto acessível separado, **GetObjectForChild** deve criar um objeto separado para cada filho sob demanda.

A implementação de exemplo a seguir retorna um objeto acessível para um item em uma exibição de lista personalizada.


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



Para obter uma implementação de exemplo completa, consulte [tornando os controles personalizados acessíveis, parte 5: usando IAccessibleEx para adicionar suporte à automação da interface do usuário a um controle personalizado](/previous-versions/msdn10/cc307850(v=msdn.10)) no msdn.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia do programador do provedor de automação de interface do usuário](uiauto-providerportal.md)
</dt> </dl>

 

 