---
description: 'Para registrar um nome de par, um aplicativo deve fornecer as seguintes informações: endereço IP listPeer identityPeer nameIf um nome de par não é seguro, uma identidade é opcional.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrando um nome de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748414"
---
# <a name="registering-a-peer-name"></a><span data-ttu-id="09356-103">Registrando um nome de par</span><span class="sxs-lookup"><span data-stu-id="09356-103">Registering a Peer Name</span></span>

<span data-ttu-id="09356-104">Para registrar um nome de par, um aplicativo deve fornecer as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="09356-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="09356-105">Lista de endereços IP</span><span class="sxs-lookup"><span data-stu-id="09356-105">IP address list</span></span>
-   [<span data-ttu-id="09356-106">Identidade de par</span><span class="sxs-lookup"><span data-stu-id="09356-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="09356-107">Nome do par</span><span class="sxs-lookup"><span data-stu-id="09356-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="09356-108">Se um nome de par não for seguro, uma identidade será opcional.</span><span class="sxs-lookup"><span data-stu-id="09356-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="09356-109">Se uma identidade de par for especificada como **NULL**, o PNRP (Peer Name Resolution Protocol) usará uma identidade de par padrão interna.</span><span class="sxs-lookup"><span data-stu-id="09356-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="09356-110">Registrando um nome de par</span><span class="sxs-lookup"><span data-stu-id="09356-110">Registering a Peer Name</span></span>

<span data-ttu-id="09356-111">Depois que a lista de endereços IP, a identidade de par e o nome de par forem identificados, o aplicativo poderá registrar um nome de par chamando [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="09356-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="09356-112">Use as diretrizes nas seções a seguir deste tópico para fazer as configurações necessárias para os parâmetros **WSASetService** e a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="09356-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="09356-113">Configurando o WSASetService</span><span class="sxs-lookup"><span data-stu-id="09356-113">Configuring WSASetService</span></span>

<span data-ttu-id="09356-114">Quando um aplicativo chama [**WSASetService**](pnrp-and-wsasetservice.md), os parâmetros devem ser configurados de acordo com as especificações a seguir:</span><span class="sxs-lookup"><span data-stu-id="09356-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="09356-115">*essOperation* deve ter um valor de **\_ registro RNRSERVICE**.</span><span class="sxs-lookup"><span data-stu-id="09356-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="09356-116">*dwFlags* deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="09356-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="09356-117">*lpqsRegInfo* deve apontar para uma estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que deve ser configurada usando as diretrizes na seção **Configurando WSAQUERYSET** a seguir deste tópico.</span><span class="sxs-lookup"><span data-stu-id="09356-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="09356-118">Configurando o WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="09356-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="09356-119">A estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve ser configurada de acordo com as especificações a seguir:</span><span class="sxs-lookup"><span data-stu-id="09356-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="09356-120">**dwSize** deve especificar o tamanho da estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="09356-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="09356-121">**lpszServiceInstanceName** deve apontar para o nome de par que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="09356-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="09356-122">**lpBlob** deve apontar para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="09356-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="09356-123">**lpcsaBuffer** deve apontar para a lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="09356-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="09356-124">Os membros restantes são descritos em [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="09356-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="09356-125">Depois que um nome de par é registrado, as informações ficam disponíveis para a infraestrutura de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="09356-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="09356-126">No entanto, há um atraso entre o tempo de registro e a propagação das informações de registro para outros nós.</span><span class="sxs-lookup"><span data-stu-id="09356-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="09356-127">Durante esse tempo, outros nós talvez não consigam resolver o par registrado recentemente.</span><span class="sxs-lookup"><span data-stu-id="09356-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="09356-128">Exemplo de registro de um nome de par</span><span class="sxs-lookup"><span data-stu-id="09356-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="09356-129">O trecho de código a seguir mostra como registrar um nome de par fornecendo as informações corretas ao chamar [**WSASetService**](pnrp-and-wsasetservice.md) usando a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="09356-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



