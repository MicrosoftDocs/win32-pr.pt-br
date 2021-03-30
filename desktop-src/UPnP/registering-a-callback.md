---
title: Registrando um retorno de chamada
description: Se o aplicativo exigir notificação quando o valor de uma variável de estado for alterado ou a instância de serviço que ele representa se tornar indisponível, o aplicativo deverá registrar uma função de retorno de chamada.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641298"
---
# <a name="registering-a-callback"></a>Registrando um retorno de chamada

Se o aplicativo exigir notificação quando o valor de uma variável de estado for alterado ou a instância de serviço que ele representa se tornar indisponível, o aplicativo deverá registrar uma função de retorno de chamada. Para registrar uma função de retorno de chamada para o objeto de serviço a ser invocado, use o método [**IUPnPService:: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Esse método pode ser usado para registrar mais de um retorno de chamada.

Os desenvolvedores não devem cancelar uma operação assíncrona dentro de um retorno de chamada assíncrono.

> [!Note]  
> Adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript. A função **GetRef** usada no VBScript não está disponível no Visual Basic. Portanto, um desenvolvedor deve criar um objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenha a função de retorno de chamada como o método padrão. Consulte [registrando um retorno de chamada no Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>Exemplo de VBScript

O código VBScript a seguir define a função de retorno de chamada **serviceChangeCallback**, a ser invocada quando os valores de variáveis de estado forem alterados ou quando a instância do serviço ficar indisponível. A função tem quatro argumentos.

O primeiro argumento para a função especifica o motivo pelo qual o retorno de chamada é invocado. Ele é invocado porque uma variável de estado foi alterada ou porque a instância do serviço tornou-se indisponível.

O segundo argumento é o objeto de serviço para o qual o retorno de chamada é invocado. Se o retorno de chamada for invocado para uma alteração de variável de estado, a função será passada com dois argumentos adicionais: o nome da variável que foi alterada e seu novo valor.

Neste exemplo, o retorno de chamada exibe apenas uma caixa de mensagem que mostra o nome da variável alterada e seu novo valor, e se o retorno de chamada foi invocado para uma alteração de variável de estado. Caso contrário, ele exibirá uma mensagem indicando que a instância do serviço não está mais disponível.

A última parte do fragmento de código mostra como registrar a função de retorno de chamada usando o método [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . As variáveis de objeto de serviço, *appService* e *xportService* , devem ter sido inicializadas, conforme mostrado em [obtendo objetos de serviço](obtaining-service-objects.md).


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a>Exemplo de C++


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 