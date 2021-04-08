---
description: Quando você cancela o registro de um nome de par, um nome registrado é removido de uma nuvem PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Cancelando o registro de um nome de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921759"
---
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="7e103-103">Cancelando o registro de um nome de par</span><span class="sxs-lookup"><span data-stu-id="7e103-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="7e103-104">Quando você cancela o registro de um nome de par, um nome registrado é removido de uma nuvem PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="7e103-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="7e103-105">Cancelando o registro de um nome de par</span><span class="sxs-lookup"><span data-stu-id="7e103-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="7e103-106">Para cancelar o registro de um nome de par, chame [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="7e103-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="7e103-107">O parâmetro *essOperation* deve ter um valor de **RNRSERVICE \_ delete**.</span><span class="sxs-lookup"><span data-stu-id="7e103-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="7e103-108">Use as diretrizes nas seções a seguir deste tópico para fazer as configurações necessárias para os parâmetros **WSASetService** e a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="7e103-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="7e103-109">Configurando o WSASetService</span><span class="sxs-lookup"><span data-stu-id="7e103-109">Configuring WSASetService</span></span>

<span data-ttu-id="7e103-110">Quando um aplicativo chama [**WSASetService**](pnrp-and-wsasetservice.md), os parâmetros devem ser configurados de acordo com as especificações a seguir:</span><span class="sxs-lookup"><span data-stu-id="7e103-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="7e103-111">*essOperation* deve ter um valor de **RNRSERVICE \_ delete**.</span><span class="sxs-lookup"><span data-stu-id="7e103-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="7e103-112">*dwFlags* deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="7e103-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="7e103-113">*lpqsRegInfo* deve apontar para uma estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que deve ser configurada usando as diretrizes na seção a seguir deste tópico.</span><span class="sxs-lookup"><span data-stu-id="7e103-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="7e103-114">Configurando o WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="7e103-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="7e103-115">A estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve ser configurada de acordo com as especificações a seguir:</span><span class="sxs-lookup"><span data-stu-id="7e103-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="7e103-116">**dwSize** deve especificar o tamanho da estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="7e103-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="7e103-117">**lpszServiceInstanceName** deve apontar para o nome de par que está sendo cancelado.</span><span class="sxs-lookup"><span data-stu-id="7e103-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="7e103-118">**lpBlob** deve apontar para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="7e103-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="7e103-119">**lpcsaBuffer** deve apontar para a lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="7e103-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="7e103-120">Os membros restantes são descritos em [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="7e103-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="7e103-121">Um exemplo de cancelamento do registro de um nome de par</span><span class="sxs-lookup"><span data-stu-id="7e103-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="7e103-122">O trecho de código a seguir mostra como cancelar o registro de um nome de par fornecendo as informações corretas ao chamar [**WSASetService**](pnrp-and-wsasetservice.md) usando a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="7e103-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



