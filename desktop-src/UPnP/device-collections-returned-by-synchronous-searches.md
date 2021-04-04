---
title: Coleções de dispositivos retornadas por pesquisas síncronas
description: Coleções de dispositivos são objetos que contêm um ou mais objetos de dispositivo. Uma coleção de dispositivos expõe a interface IUPnPDevices que fornece métodos e propriedades para percorrer a coleção e extrair objetos de dispositivo individuais.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084749"
---
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="4591c-104">Coleções de dispositivos retornadas por pesquisas síncronas</span><span class="sxs-lookup"><span data-stu-id="4591c-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="4591c-105">Coleções de dispositivos são objetos que contêm um ou mais objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4591c-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="4591c-106">Uma coleção de dispositivos expõe a interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) que fornece métodos e propriedades para percorrer a coleção e extrair objetos de dispositivo individuais.</span><span class="sxs-lookup"><span data-stu-id="4591c-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="4591c-107">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="4591c-107">VBScript Example</span></span>

<span data-ttu-id="4591c-108">Os aplicativos VBScript podem acessar os objetos na coleção de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="4591c-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="4591c-109">Primeiro, eles podem atravessar os elementos sequencialmente usando um para...</span><span class="sxs-lookup"><span data-stu-id="4591c-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="4591c-110">cada... Next, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="4591c-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="4591c-111">Neste exemplo, presume-se que a variável de dispositivos tenha sido inicializada com o resultado de uma pesquisa anterior.</span><span class="sxs-lookup"><span data-stu-id="4591c-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="4591c-112">O loop percorre os objetos de dispositivo na coleção, atribuindo a variável deviceObj o valor de cada objeto de dispositivo por vez.</span><span class="sxs-lookup"><span data-stu-id="4591c-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="4591c-113">O corpo do loop pode conter código que processa o objeto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4591c-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="4591c-114">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="4591c-114">C++ Example</span></span>

<span data-ttu-id="4591c-115">O exemplo a seguir mostra o código C++ necessário para acessar os objetos em uma coleção de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4591c-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="4591c-116">A função mostrada, **TraverseCollection**, recebe um ponteiro para a interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="4591c-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="4591c-117">Esse ponteiro de interface pode ser retornado pelo método [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) , ou outros métodos **Find** , do objeto localizador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4591c-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



<span data-ttu-id="4591c-118">A primeira etapa é solicitar um novo enumerador para a coleção usando a propriedade [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="4591c-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="4591c-119">Isso retorna um enumerador como a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4591c-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4591c-120">O código de exemplo chama [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter a interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="4591c-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="4591c-121">Em seguida, o código de exemplo define o enumerador como o início da coleção invocando o método [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) .</span><span class="sxs-lookup"><span data-stu-id="4591c-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="4591c-122">Por fim, o código de exemplo invoca o método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para atravessar a coleção.</span><span class="sxs-lookup"><span data-stu-id="4591c-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="4591c-123">Os objetos de dispositivo na coleção estão contidos em estruturas de **variante** .</span><span class="sxs-lookup"><span data-stu-id="4591c-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="4591c-124">Essas estruturas contêm ponteiros para interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nos objetos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4591c-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="4591c-125">Para obter a interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , o código de exemplo invoca **QueryInterface** na interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="4591c-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 