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
# <a name="invoking-actions"></a>Invocando ações

O método [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permite que as ações sejam invocadas em objetos de serviço. Esse método tem dois parâmetros de entrada: o nome de uma ação e uma matriz de argumentos de entrada para essa ação. O método tem dois parâmetros:

-   Parameter um — um parâmetro de entrada/saída: uma matriz de argumentos de saída para essa ação.
-   Parâmetro dois — um parâmetro de saída: um valor de retorno.

O método faz com que a ação seja invocada no dispositivo. O dispositivo gerará notificações de eventos se a ação fizer com que as variáveis de estado do dispositivo sejam alteradas.

## <a name="vbscript-example"></a>Exemplo de VBScript

O exemplo de código VBScript a seguir invoca duas ações em um objeto de serviço. A primeira ação, *GetTrackInfo*, usa um argumento de entrada, um número de faixa. A ação *GetTrackInfo* retorna o comprimento da faixa como o valor de retorno. A ação também tem um argumento de saída, que contém o título da faixa se o método retornar êxito.

Depois de invocar a ação *GetTrackInfo* , o exemplo invoca a ação Play, que não usa nenhum argumento. No entanto, como a sintaxe de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requer uma matriz de argumentos de entrada e saída, o exemplo deve criar uma matriz vazia, *emptyArgs*, sem elementos. O exemplo passa essa matriz para **InvokeAction** para os argumentos de entrada e saída, juntamente com o nome da ação.


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



## <a name="c-example"></a>Exemplo de C++

O exemplo a seguir define uma função C++ que invoca uma ação sem argumentos. Como [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) exige que um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de argumentos seja passado, este exemplo cria um **SafeArray** vazio. Como essa ação não retorna um valor ou tem argumentos de saída, este exemplo ignora os últimos dois valores [**variantes**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passados para **InvokeAction**.

O dispositivo gerará notificações de eventos se a ação fizer com que as variáveis de estado do dispositivo sejam alteradas.


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



O exemplo a seguir invoca a ação *GetTrackInfo* fictícia. Ele usa um número de faixa como um argumento, retorna o comprimento da faixa como um valor de retorno e retorna o título da faixa em um argumento de saída. O código é semelhante ao exemplo anterior, exceto que, em vez de criar um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) vazio de argumentos de entrada, este exemplo insere uma [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) que contém o número de faixa. Se [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) retornar êxito, este exemplo examinará o valor de retorno e a matriz de argumentos de saída.


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



 

 