---
title: Invocando ações
description: O método IUPnPService InvokeAction permite que as ações sejam invocadas em objetos de serviço.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366457"
---
# <a name="invoking-actions"></a><span data-ttu-id="2c5ca-103">Invocando ações</span><span class="sxs-lookup"><span data-stu-id="2c5ca-103">Invoking Actions</span></span>

<span data-ttu-id="2c5ca-104">O método [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permite que as ações sejam invocadas em objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="2c5ca-105">Esse método tem dois parâmetros de entrada: o nome de uma ação e uma matriz de argumentos de entrada para essa ação.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="2c5ca-106">O método tem dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="2c5ca-106">The method has two parameters:</span></span>

-   <span data-ttu-id="2c5ca-107">Parameter um — um parâmetro de entrada/saída: uma matriz de argumentos de saída para essa ação.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="2c5ca-108">Parâmetro dois — um parâmetro de saída: um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="2c5ca-109">O método faz com que a ação seja invocada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="2c5ca-110">O dispositivo gerará notificações de eventos se a ação fizer com que as variáveis de estado do dispositivo sejam alteradas.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="2c5ca-111">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="2c5ca-111">VBScript Example</span></span>

<span data-ttu-id="2c5ca-112">O exemplo de código VBScript a seguir invoca duas ações em um objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="2c5ca-113">A primeira ação, *GetTrackInfo*, usa um argumento de entrada, um número de faixa.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="2c5ca-114">A ação *GetTrackInfo* retorna o comprimento da faixa como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="2c5ca-115">A ação também tem um argumento de saída, que contém o título da faixa se o método retornar êxito.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="2c5ca-116">Depois de invocar a ação *GetTrackInfo* , o exemplo invoca a ação Play, que não usa nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="2c5ca-117">No entanto, como a sintaxe de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requer uma matriz de argumentos de entrada e saída, o exemplo deve criar uma matriz vazia, *emptyArgs*, sem elementos.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="2c5ca-118">O exemplo passa essa matriz para **InvokeAction** para os argumentos de entrada e saída, juntamente com o nome da ação.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a><span data-ttu-id="2c5ca-119">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="2c5ca-119">C++ Example</span></span>

<span data-ttu-id="2c5ca-120">O exemplo a seguir define uma função C++ que invoca uma ação sem argumentos.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="2c5ca-121">Como [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) exige que um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de argumentos seja passado, este exemplo cria um **SafeArray** vazio.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="2c5ca-122">Como essa ação não retorna um valor ou tem argumentos de saída, este exemplo ignora os últimos dois valores [**variantes**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passados para **InvokeAction**.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="2c5ca-123">O dispositivo gerará notificações de eventos se a ação fizer com que as variáveis de estado do dispositivo sejam alteradas.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



<span data-ttu-id="2c5ca-124">O exemplo a seguir invoca a ação *GetTrackInfo* fictícia.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="2c5ca-125">Ele usa um número de faixa como um argumento, retorna o comprimento da faixa como um valor de retorno e retorna o título da faixa em um argumento de saída.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="2c5ca-126">O código é semelhante ao exemplo anterior, exceto que, em vez de criar um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) vazio de argumentos de entrada, este exemplo insere uma [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) que contém o número de faixa.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="2c5ca-127">Se [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) retornar êxito, este exemplo examinará o valor de retorno e a matriz de argumentos de saída.</span><span class="sxs-lookup"><span data-stu-id="2c5ca-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 