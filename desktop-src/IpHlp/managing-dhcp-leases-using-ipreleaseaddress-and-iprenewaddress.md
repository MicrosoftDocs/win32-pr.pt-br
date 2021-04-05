---
title: Gerenciar concessões de DHCP com IpReleaseAddress, IpRenewAddress
description: As funções IpReleaseAddress e IpRenewAddress são usadas para liberar e renovar a concessão de DHCP (protocolo de configuração dinâmica de hosts) atual.
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827049"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="33e82-103">Gerenciar concessões de DHCP com IpReleaseAddress, IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="33e82-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="33e82-104">As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) são usadas para liberar e renovar a concessão de DHCP (protocolo de configuração dinâmica de hosts) atual.</span><span class="sxs-lookup"><span data-stu-id="33e82-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="33e82-105">A função **IpReleaseAddress** libera um endereço IPv4 obtido anteriormente por meio do DHCP.</span><span class="sxs-lookup"><span data-stu-id="33e82-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="33e82-106">A função **IpRenewAddress** renova uma concessão em um endereço IPv4 obtido anteriormente por meio do DHCP.</span><span class="sxs-lookup"><span data-stu-id="33e82-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="33e82-107">É comum usar essas duas funções juntas, primeiro liberando a concessão com uma chamada para **IpReleaseAddress** e, em seguida, renovando a concessão com uma chamada para a função **IpRenewAddress** .</span><span class="sxs-lookup"><span data-stu-id="33e82-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="33e82-108">Quando um cliente DHCP tiver obtido anteriormente uma concessão DHCP e [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) não for chamado antes da função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , a solicitação do cliente DHCP será enviada ao servidor DHCP que emitiu a concessão de DHCP inicial.</span><span class="sxs-lookup"><span data-stu-id="33e82-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="33e82-109">Esse servidor DHCP pode não estar disponível ou a solicitação DHCP pode falhar.</span><span class="sxs-lookup"><span data-stu-id="33e82-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="33e82-110">Quando um host tiver obtido anteriormente uma concessão DHCP e **IpReleaseAddress** for chamado antes da função **IpRenewAddress** , o cliente DHCP primeiro liberará o endereço IP obtido e enviará uma solicitação de cliente DHCP para uma resposta de qualquer servidor DHCP disponível.</span><span class="sxs-lookup"><span data-stu-id="33e82-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="33e82-111">As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) exigem que o DHCP esteja habilitado para ser executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="33e82-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="33e82-112">A função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) usa um ponteiro para uma estrutura de mapa de [**índice de \_ adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) como seu único parâmetro.</span><span class="sxs-lookup"><span data-stu-id="33e82-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="33e82-113">Para obter esse parâmetro, primeiro chame [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span><span class="sxs-lookup"><span data-stu-id="33e82-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="33e82-114">Para obter ajuda com a função **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="33e82-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="33e82-115">**Para usar o IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="33e82-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="33e82-116">Obtenha um ponteiro para uma estrutura de [**mapa de \_ índice de adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) usando a função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="33e82-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="33e82-117">(Para obter ajuda com a função GetInterfaceInfo, consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="33e82-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="33e82-118">Crie um  objeto DWORD `dwRetVal` (usado para verificação de erro).</span><span class="sxs-lookup"><span data-stu-id="33e82-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="33e82-119">Supõe-se que a variável retornada por **GetInterfaceInfo** seja chamada `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="33e82-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="33e82-120">Se o DHCP estiver habilitado, chame a função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , passando a variável de [**mapa de \_ índice do adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como seu parâmetro.</span><span class="sxs-lookup"><span data-stu-id="33e82-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="33e82-121">Verifique se há erros gerais e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).</span><span class="sxs-lookup"><span data-stu-id="33e82-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="33e82-122">A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retorna um parâmetro que pode ser usado para verificar se o DHCP está habilitado antes de chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="33e82-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="33e82-123">Para obter ajuda com o **GetAdaptersInfo**, consulte [Gerenciando adaptadores de rede usando o GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="33e82-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="33e82-124">É comum usar essas duas funções juntas, chamar a função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e, em seguida, chamar a função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando a mesma estrutura que o parâmetro para ambas as funções.</span><span class="sxs-lookup"><span data-stu-id="33e82-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="33e82-125">O procedimento a seguir pressupõe que as funções não são usadas juntas; no entanto, se as funções forem usadas juntas, pule a etapa 1.</span><span class="sxs-lookup"><span data-stu-id="33e82-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="33e82-126">**Para usar o IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="33e82-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="33e82-127">Obtenha um ponteiro para uma estrutura de [**mapa de \_ índice de adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) usando a função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="33e82-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="33e82-128">(Para obter ajuda com a função **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span><span class="sxs-lookup"><span data-stu-id="33e82-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="33e82-129">Declare um  objeto DWORD `dwRetVal` (usado para verificação de erro) se essa variável não tiver sido declarada.</span><span class="sxs-lookup"><span data-stu-id="33e82-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="33e82-130">Supõe-se que a variável retornada por **GetInterfaceInfo** seja chamada `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="33e82-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="33e82-131">Chame a função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando a variável de mapa de [**\_ \_ índice \_ do adaptador IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como seu parâmetro.</span><span class="sxs-lookup"><span data-stu-id="33e82-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="33e82-132">Verifique se há erros gerais e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).</span><span class="sxs-lookup"><span data-stu-id="33e82-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="33e82-133">Próxima etapa: [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="33e82-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="33e82-134">Etapa anterior: [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="33e82-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



