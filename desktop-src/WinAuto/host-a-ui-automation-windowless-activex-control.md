---
title: Hospedar um controle ActiveX sem janela de automação da interface do usuário
description: Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam a automação da interface do usuário da Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automação da interface do usuário, controle ActiveX sem janela
- Controle ActiveX sem janela, automação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294111"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>Hospedar um controle ActiveX sem janela de automação da interface do usuário

Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam a automação da interface do usuário da Microsoft. Usando as etapas descritas aqui, você pode garantir que qualquer controle sem janela da automação da interface do usuário hospedado em seu contêiner de controle seja acessível a aplicativos cliente de tecnologia assistencial (AT).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Automação da Interface do Usuário](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação do COM (Microsoft Win32 e Component Object Model)
-   Controles ActiveX sem janela
-   Provedores de automação da interface do usuário

## <a name="instructions"></a>Instruções

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Etapa 1: forneça a interface IRawElementProviderSimple em nome do controle sem janela.

Sempre que o sistema precisar do ponteiro [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para a raiz de um controle sem janela, o sistema consultará o contêiner de controle. Para recuperar o ponteiro, o contêiner chama a implementação de controle sem janela do método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Se o contêiner de controle tiver uma implementação de automação de interface do usuário, ele poderá retornar o ponteiro [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do controle sem janela para o sistema.

Se o contêiner de controle tiver uma implementação de Acessibilidade Ativa da Microsoft, chame a função [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) para obter um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que represente o controle e, em seguida, retorne o ponteiro da interface **IAccessible** para o sistema.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Etapa 2: implementar a interface IRawElementProviderWindowlessSite.

Um contêiner de controle implementa a interface [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) habilita um controle sem janela baseado na automação da interface do usuário para comunicar suas informações de acessibilidade.

1.  Implemente [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Um fragmento de controle sem janela deve criar uma ID de tempo de execução exclusiva para si mesmo. Para criar sua ID de tempo de execução, um fragmento de controle sem janela recupera um valor de prefixo chamando o método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) do site de controle e, em seguida, acrescenta ao prefixo um valor inteiro que é exclusivo em relação a todos os outros fragmentos no controle sem janela.

    O site de controle para um controle sem janela deve implementar o método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) formando um **SafeArray** que contém a constante **UiaAppendRuntimeId**, seguido por um valor inteiro que é exclusivo para o site.

    Este exemplo mostra como retornar um prefixo de ID de tempo de execução para um controle sem janela.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  Implemente o método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .

    Um controle que implementa a automação da interface do usuário deve retornar um ponteiro para o provedor de fragmento pai do controle.

    Para retornar o pai do fragmento, um objeto que implementa a interface [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) deve ser capaz de implementar o método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) . A implementação de **Navigate** é difícil para um controle sem janela porque o controle pode não conseguir determinar seu local na árvore acessível do objeto pai. O método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permite que o controle sem janela consulte seu site para o fragmento adjacente e, em seguida, retorne esse fragmento para o cliente que chamou **Navigate**.

    Este exemplo mostra como um contêiner de controle recupera o fragmento pai de um controle sem janela.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Etapa 3: opcional: implementar a interface IRawElementProviderHostingAccessibles.

Implemente a interface [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) se o seu contêiner de controle tiver uma implementação de provedor de automação de interface do usuário que seja a raiz de uma árvore de acessibilidade que inclui controles ActiveX sem janela que dão suporte ao Microsoft acessibilidade ativa. A interface **IRawElementProviderHostingAccessibles** tem um método único, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), que recupera os ponteiros da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de todos os controles ActiveX sem janela baseados no Microsoft acessibilidade ativa que são hospedados pelo seu contêiner de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como hospedar um controle ActiveX sem janela do MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[Acessibilidade de controle ActiveX sem janela](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 