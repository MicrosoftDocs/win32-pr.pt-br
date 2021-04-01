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
# <a name="registering-a-callback"></a><span data-ttu-id="56681-103">Registrando um retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="56681-103">Registering a Callback</span></span>

<span data-ttu-id="56681-104">Se o aplicativo exigir notificação quando o valor de uma variável de estado for alterado ou a instância de serviço que ele representa se tornar indisponível, o aplicativo deverá registrar uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="56681-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="56681-105">Para registrar uma função de retorno de chamada para o objeto de serviço a ser invocado, use o método [**IUPnPService:: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="56681-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="56681-106">Esse método pode ser usado para registrar mais de um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="56681-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="56681-107">Os desenvolvedores não devem cancelar uma operação assíncrona dentro de um retorno de chamada assíncrono.</span><span class="sxs-lookup"><span data-stu-id="56681-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="56681-108">Adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript.</span><span class="sxs-lookup"><span data-stu-id="56681-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="56681-109">A função **GetRef** usada no VBScript não está disponível no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="56681-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="56681-110">Portanto, um desenvolvedor deve criar um objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenha a função de retorno de chamada como o método padrão.</span><span class="sxs-lookup"><span data-stu-id="56681-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="56681-111">Consulte [registrando um retorno de chamada no Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="56681-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="56681-112">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="56681-112">VBScript Example</span></span>

<span data-ttu-id="56681-113">O código VBScript a seguir define a função de retorno de chamada **serviceChangeCallback**, a ser invocada quando os valores de variáveis de estado forem alterados ou quando a instância do serviço ficar indisponível.</span><span class="sxs-lookup"><span data-stu-id="56681-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="56681-114">A função tem quatro argumentos.</span><span class="sxs-lookup"><span data-stu-id="56681-114">The function has four arguments.</span></span>

<span data-ttu-id="56681-115">O primeiro argumento para a função especifica o motivo pelo qual o retorno de chamada é invocado.</span><span class="sxs-lookup"><span data-stu-id="56681-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="56681-116">Ele é invocado porque uma variável de estado foi alterada ou porque a instância do serviço tornou-se indisponível.</span><span class="sxs-lookup"><span data-stu-id="56681-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="56681-117">O segundo argumento é o objeto de serviço para o qual o retorno de chamada é invocado.</span><span class="sxs-lookup"><span data-stu-id="56681-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="56681-118">Se o retorno de chamada for invocado para uma alteração de variável de estado, a função será passada com dois argumentos adicionais: o nome da variável que foi alterada e seu novo valor.</span><span class="sxs-lookup"><span data-stu-id="56681-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="56681-119">Neste exemplo, o retorno de chamada exibe apenas uma caixa de mensagem que mostra o nome da variável alterada e seu novo valor, e se o retorno de chamada foi invocado para uma alteração de variável de estado.</span><span class="sxs-lookup"><span data-stu-id="56681-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="56681-120">Caso contrário, ele exibirá uma mensagem indicando que a instância do serviço não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="56681-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="56681-121">A última parte do fragmento de código mostra como registrar a função de retorno de chamada usando o método [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="56681-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="56681-122">As variáveis de objeto de serviço, *appService* e *xportService* , devem ter sido inicializadas, conforme mostrado em [obtendo objetos de serviço](obtaining-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="56681-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


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



## <a name="c-example"></a><span data-ttu-id="56681-123">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="56681-123">C++ Example</span></span>


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



 

 