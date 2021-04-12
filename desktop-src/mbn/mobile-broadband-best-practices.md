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
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="bd3a7-103">Práticas recomendadas da API de banda larga móvel</span><span class="sxs-lookup"><span data-stu-id="bd3a7-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="bd3a7-104">Ao trabalhar com a API de banda larga móvel, o seguinte conjunto de práticas recomendadas deve ser usado para alcançar o melhor desempenho possível.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="bd3a7-105">Não armazenar objetos funcionais em cache</span><span class="sxs-lookup"><span data-stu-id="bd3a7-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="bd3a7-106">Os objetos funcionais, como [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) e outros, são obtidos de objetos Manager, como [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), usando o método Enumeration no objeto Manager correspondente.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="bd3a7-107">Não armazene em cache esses objetos funcionais, pois os objetos funcionais armazenados em cache contêm dados obsoletos.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="bd3a7-108">As operações síncronas executadas nesses objetos funcionais retornarão os mesmos dados até que os objetos funcionais sejam obtidos novamente.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="bd3a7-109">Em vez disso, armazene em cache os objetos de Gerenciador e obtenha os objetos funcionais do objeto de Gerenciador usando o método de enumeração no objeto de Gerenciador correspondente novamente para obter os dados mais recentes.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="bd3a7-110">O exemplo de código a seguir demonstra a maneira apropriada de armazenar objetos do Gerenciador de cache.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


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



## <a name="handle-all-notifications"></a><span data-ttu-id="bd3a7-111">Lidar com todas as notificações</span><span class="sxs-lookup"><span data-stu-id="bd3a7-111">Handle All Notifications</span></span>

<span data-ttu-id="bd3a7-112">Siga e manipule todas as notificações, mesmo que elas não sejam disparadas pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="bd3a7-113">Isso é necessário para manter a interface do usuário em sincronia com o estado real do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="bd3a7-114">Pode haver mais de um Gerenciador de conexões em execução em um computador.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="bd3a7-115">O modo de exibição nativo da interface de rede disponível fornecida pelo Windows 7 é um Gerenciador de conexões.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="bd3a7-116">Quaisquer outros gerenciadores de conexões precisam responder a todas as notificações para permanecerem em sincronia com a interface do usuário nativa do Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="bd3a7-117">Um usuário pode optar por executar alguma operação em um dos gerenciadores de conexões, o que pode resultar em uma alteração de estado do dispositivo de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="bd3a7-118">No entanto, outros gerenciadores de conexões precisam permanecer atualizados para indicar corretamente o estado modificado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="bd3a7-119">Por exemplo, a execução de uma conexão usando um dos gerenciadores de conexões alterará o estado do dispositivo de disponível para conectado.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="bd3a7-120">Essa alteração deve ser visível para os gerenciadores de conexões que não iniciaram essa ação.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="bd3a7-121">Todos os gerenciadores de conexões que têm a interface do usuário que indica o estado de conexão do dispositivo, precisam escutar e manipular as notificações de estado da conexão para atualizar corretamente sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="bd3a7-122">Enviando e recebendo bytes</span><span class="sxs-lookup"><span data-stu-id="bd3a7-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="bd3a7-123">Use as funções auxiliares de IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) e [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) para enviar e receber bytes.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="bd3a7-124">Usando a API de desbloqueio de PIN</span><span class="sxs-lookup"><span data-stu-id="bd3a7-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="bd3a7-125">Um aplicativo cliente de chamada deve ser elevado para invocar com êxito o [**IMbnPin:: desbloquear**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span><span class="sxs-lookup"><span data-stu-id="bd3a7-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="bd3a7-126">Esse método é a única parte da API de banda larga móvel que exige privilégios de administrador ou NCO.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="bd3a7-127">Consulte [uma descrição do grupo operadores de configuração de rede]( https://support.microsoft.com/kb/297938/en-us) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="bd3a7-128">Trabalhando com SafeArrays</span><span class="sxs-lookup"><span data-stu-id="bd3a7-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="bd3a7-129">Use ZeroMemory () antes de acessar quaisquer elementos em um SafeArray.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="bd3a7-130">Não verifique os índices de um SafeArray.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="bd3a7-131">Eles podem ser negativos.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-131">They may be negative.</span></span>

<span data-ttu-id="bd3a7-132">O exemplo de código a seguir mostra como lidar corretamente com um SafeArray.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-132">The following code example shows how to properly handle a SafeArray.</span></span>


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



 

 
