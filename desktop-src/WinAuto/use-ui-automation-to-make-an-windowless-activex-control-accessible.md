---
title: como usar a automação da interface do usuário para tornar um controle de ActiveX sem janelas acessível
description: Descreve como usar a automação da interface do usuário da Microsoft \ 32; API para garantir que o controle de ActiveX da Microsoft sem janelas esteja acessível para aplicativos cliente de tecnologia assistencial (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- controle de ActiveX sem janela, acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570356"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>como usar a automação da interface do usuário para tornar um controle de ActiveX sem janelas acessível

descreve como usar a API de automação da interface do usuário da microsoft para garantir que o controle da microsoft ActiveX sem janelas seja acessível a aplicativos cliente de tecnologia assistencial (AT).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [ActiveX Controles](/windows/desktop/com/activex-controls)
-   [Automação da Interface do Usuário](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação do COM (Microsoft Win32 e Component Object Model)
-   controles de ActiveX sem janela
-   Provedores de automação da interface do usuário

## <a name="instructions"></a>Instruções

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Etapa 1: implementar as interfaces do provedor de automação da interface do usuário.

para tornar seu aplicativo acessível, você deve implementar as interfaces do provedor de automação da interface do usuário para o controle de ActiveX sem janela, incluindo [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). Você deve implementar essas interfaces da mesma forma como faria para um controle baseado em janela, exceto conforme descrito nas etapas a seguir. Para obter mais informações sobre como implementar interfaces de provedor UIA, consulte [Guia do programador do provedor de automação de IU](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Etapa 2: implementar a interface IServiceProvider.

Quando um cliente precisa de informações de acessibilidade sobre o controle sem janela, o contêiner de controle chama o método **IServiceProvider:: QueryService** do controle para recuperar o ponteiro de interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para seu controle.

O exemplo a seguir mostra como implementar o método **QueryService** .


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Etapa 3: implementar o método IRawElementProviderFragment:: Navigate.

Quando o método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) do controle sem janela é chamado para navegar até o pai ou um irmão do provedor raiz do controle sem janela, seu método **Navigate** deve delegar ao método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) do contêiner de controle.

O exemplo a seguir mostra como implementar o método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Etapa 4: implementar o método IRawElementProviderFragment:: GetRuntimeId.

Quando o controle sem janela recebe uma chamada para o método [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , o controle deve fazer o seguinte:

1.  Recupere um prefixo de ID de tempo de execução chamando o método [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) do site de controle.
2.  Crie uma ID de tempo de execução exclusiva para o controle acrescentando um inteiro ao prefixo de ID de tempo de execução.
3.  Retornar a ID de tempo de execução para o chamador.

O exemplo a seguir mostra como implementar o método [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Use a MSAA para tornar um controle de ActiveX sem janela acessível](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[acessibilidade de controle de ActiveX sem janelas](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 