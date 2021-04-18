---
title: Usar MSAA para tornar um controle ActiveX sem janela acessível
description: Descreve como usar o Microsoft Acessibilidade Ativa \ 32; API para garantir que o controle Microsoft ActiveX sem janela esteja acessível para aplicativos cliente de tecnologia assistencial (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Controle ActiveX, acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813717"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Usar MSAA para tornar um controle ActiveX sem janela acessível

Descreve como usar a API do Microsoft Acessibilidade Ativa para garantir que o controle Microsoft ActiveX sem janela esteja acessível para aplicativos cliente de tecnologia assistencial (AT).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Acessibilidade Ativa da Microsoft](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação do COM (Microsoft Win32 e Component Object Model)
-   Controles ActiveX sem janela
-   Servidores Microsoft Acessibilidade Ativa

## <a name="instructions"></a>Instruções

### <a name="step-1-implement-the-iaccessible-interface"></a>Etapa 1: implementar a interface IAccessible.

Para tornar o controle ActiveX sem janela acessível, você deve implementar a interface do Microsoft Acessibilidade Ativa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , assim como faria com um controle baseado em janela, exceto conforme descrito nas etapas a seguir. Para obter mais informações sobre como implementar o **IAccessible**, consulte o [Guia do desenvolvedor para servidores de acessibilidade ativa](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Etapa 2: implementar a interface IServiceProvider.

Quando um cliente solicita informações de acessibilidade sobre o controle sem janela, o contêiner chama o método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) do controle para recuperar o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Este exemplo mostra como implementar o método [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Etapa 3: delegar o IAccessible:: get \_ accParent chamadas de método para o método IAccessibleWindowlessSite:: GetParentAccessible do site de controle.

Quando um cliente solicita o objeto pai do controle sem janela, o contêiner chama o método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) do seu controle. Sua implementação de **Get \_ accParent** deve delegar ao método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) do contêiner.

Este exemplo mostra como implementar o método [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Etapa 4: adquirir um intervalo de IDs de objeto para atribuir às fontes de evento no controle sem janela.

Assim como os controles baseados em janela, um controle ActiveX sem janela chama a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar os clientes sobre eventos importantes. Os parâmetros de função incluem a ID de objeto do item que está gerando o evento. O controle sem janela deve atribuir IDs de objeto usando um valor de um intervalo adquirido chamando o método [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) do site de controle.

Este exemplo mostra como adquirir um intervalo de valores de ID de objeto do contêiner de controle.


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Etapa 5: implementar a interface IAccessibleHandler.

Quando um controle sem janela chama a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , o controle Especifica a ID de objeto do item da interface do usuário que está gerando o evento e especifica o contêiner de controle como a janela que responderá às mensagens do [**WM \_ GetObject**](wm-getobject.md) em nome do controle.

Se um aplicativo cliente responder ao evento, o contêiner de controle receberá uma mensagem do [**WM \_ GetObject**](wm-getobject.md) que inclui a ID de objeto do item da interface do usuário que gerou o evento. O contêiner de controle responde pesquisando o controle sem janela que "possui" a ID de objeto e, em seguida, chamando o método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) do controle. O método **AccessibleObjectFromID** retorna o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o item da interface do usuário e o contêiner de controle encaminha o ponteiro para o aplicativo cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Acessibilidade de controle ActiveX sem janela](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 