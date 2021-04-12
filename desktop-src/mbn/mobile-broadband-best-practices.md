---
description: Ao trabalhar com a API de banda larga móvel, o seguinte conjunto de práticas recomendadas deve ser usado para alcançar o melhor desempenho possível.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Práticas recomendadas da API de banda larga móvel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164578"
---
# <a name="mobile-broadband-api-best-practices"></a>Práticas recomendadas da API de banda larga móvel

Ao trabalhar com a API de banda larga móvel, o seguinte conjunto de práticas recomendadas deve ser usado para alcançar o melhor desempenho possível.

## <a name="do-not-cache-functional-objects"></a>Não armazenar objetos funcionais em cache

Os objetos funcionais, como [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) e outros, são obtidos de objetos Manager, como [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), usando o método Enumeration no objeto Manager correspondente. Não armazene em cache esses objetos funcionais, pois os objetos funcionais armazenados em cache contêm dados obsoletos. As operações síncronas executadas nesses objetos funcionais retornarão os mesmos dados até que os objetos funcionais sejam obtidos novamente.

Em vez disso, armazene em cache os objetos de Gerenciador e obtenha os objetos funcionais do objeto de Gerenciador usando o método de enumeração no objeto de Gerenciador correspondente novamente para obter os dados mais recentes.

O exemplo de código a seguir demonstra a maneira apropriada de armazenar objetos do Gerenciador de cache.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Lidar com todas as notificações

Siga e manipule todas as notificações, mesmo que elas não sejam disparadas pelo seu aplicativo. Isso é necessário para manter a interface do usuário em sincronia com o estado real do dispositivo.

Pode haver mais de um Gerenciador de conexões em execução em um computador. O modo de exibição nativo da interface de rede disponível fornecida pelo Windows 7 é um Gerenciador de conexões. Quaisquer outros gerenciadores de conexões precisam responder a todas as notificações para permanecerem em sincronia com a interface do usuário nativa do Windows. Um usuário pode optar por executar alguma operação em um dos gerenciadores de conexões, o que pode resultar em uma alteração de estado do dispositivo de banda larga móvel. No entanto, outros gerenciadores de conexões precisam permanecer atualizados para indicar corretamente o estado modificado do dispositivo.

Por exemplo, a execução de uma conexão usando um dos gerenciadores de conexões alterará o estado do dispositivo de disponível para conectado. Essa alteração deve ser visível para os gerenciadores de conexões que não iniciaram essa ação. Todos os gerenciadores de conexões que têm a interface do usuário que indica o estado de conexão do dispositivo, precisam escutar e manipular as notificações de estado da conexão para atualizar corretamente sua interface do usuário.

## <a name="sending-and-receiving-bytes"></a>Enviando e recebendo bytes

Use as funções auxiliares de IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) e [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) para enviar e receber bytes.

## <a name="using-the-pin-unblock-api"></a>Usando a API de desbloqueio de PIN

Um aplicativo cliente de chamada deve ser elevado para invocar com êxito o [**IMbnPin:: desbloquear**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock). Esse método é a única parte da API de banda larga móvel que exige privilégios de administrador ou NCO. Consulte [uma descrição do grupo operadores de configuração de rede]( https://support.microsoft.com/kb/297938/en-us) para obter mais informações.

## <a name="working-with-safearrays"></a>Trabalhando com SafeArrays

-   Use ZeroMemory () antes de acessar quaisquer elementos em um SafeArray.

-   Não verifique os índices de um SafeArray. Eles podem ser negativos.

O exemplo de código a seguir mostra como lidar corretamente com um SafeArray.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
