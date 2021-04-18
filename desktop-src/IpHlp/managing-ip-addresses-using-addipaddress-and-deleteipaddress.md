---
title: Gerenciar endereços IP com AddIPAddress, DeleteIPAddress
description: A função AddIPAddress adiciona o endereço IPv4 especificado ao adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779914"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="1ebda-103">Gerenciar endereços IP com AddIPAddress, DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="1ebda-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="1ebda-104">A função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) adiciona o endereço IPv4 especificado ao adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="1ebda-105">A função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) exclui o endereço IPv4 especificado do adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="1ebda-106">Essas funções podem ser usadas para adicionar e excluir endereços IPv4 para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1ebda-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="1ebda-107">Um endereço IPv4 adicionado pela função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) não é persistente.</span><span class="sxs-lookup"><span data-stu-id="1ebda-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="1ebda-108">O endereço IPv4 existe somente contanto que o objeto adaptador exista.</span><span class="sxs-lookup"><span data-stu-id="1ebda-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="1ebda-109">A reinicialização do computador destrói o endereço IPv4, assim como a redefinição manual da NIC (placa de interface de rede).</span><span class="sxs-lookup"><span data-stu-id="1ebda-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="1ebda-110">Após a chamada de [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) com êxito, o DHCP será desabilitado para o endereço IP que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="1ebda-111">Portanto, funções como [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que exigem DHCP para serem habilitadas, não estarão funcionais no endereço IP adicionado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="1ebda-112">A função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) pode ser usada para excluir o endereço IPv4 adicionado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="1ebda-113">As políticas de grupo, as políticas corporativas e outras restrições na rede podem impedir que essas funções sejam concluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="1ebda-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="1ebda-114">Verifique se o aplicativo tem as permissões de rede necessárias antes de tentar usar essas funções.</span><span class="sxs-lookup"><span data-stu-id="1ebda-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="1ebda-115">**Para usar o AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="1ebda-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="1ebda-116">Declare as variáveis **ULONG** chamadas `NTEContext` e `NTEInstance` , ambas inicializadas como zero.</span><span class="sxs-lookup"><span data-stu-id="1ebda-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="1ebda-117">A `NTEContext` variável é o único parâmetro para a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; para excluir o endereço IP que é adicionado, `NTEContext` deve ser armazenado e inalterado.</span><span class="sxs-lookup"><span data-stu-id="1ebda-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="1ebda-118">Declare variáveis para as estruturas IPAddr e IPMask chamadas `iaIPAddress` e `iaIPMask` , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1ebda-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="1ebda-119">Esses valores são simplesmente números inteiros sem sinal.</span><span class="sxs-lookup"><span data-stu-id="1ebda-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="1ebda-120">Inicialize as `iaIPAddress` `iaIPMask` variáveis e usando a função de [**\_ endereço inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .</span><span class="sxs-lookup"><span data-stu-id="1ebda-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="1ebda-121">Chame a função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar o endereço IPv4.</span><span class="sxs-lookup"><span data-stu-id="1ebda-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="1ebda-122">Verifique se há erros e retorne o valor de erro para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).</span><span class="sxs-lookup"><span data-stu-id="1ebda-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="1ebda-123">O terceiro parâmetro é o índice do adaptador, que pode ser obtido chamando-se a função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="1ebda-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="1ebda-124">Supõe-se que a variável retornada por essa função é nomeada `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="1ebda-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="1ebda-125">Para obter ajuda com a função **GetIpAddrTable** , consulte [Gerenciando o endereço IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="1ebda-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="1ebda-126">**Para usar o DeleteIpAddress**</span><span class="sxs-lookup"><span data-stu-id="1ebda-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="1ebda-127">Chame a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , passando a `NTEContext` variável como seu parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1ebda-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="1ebda-128">Verifique se há erros e retorne o valor de erro para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).</span><span class="sxs-lookup"><span data-stu-id="1ebda-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="1ebda-129">Para usar [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) deve primeiro ser chamado para obter o identificador `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="1ebda-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="1ebda-130">O procedimento anterior pressupõe que **AddIPAddress** já foi chamado em algum lugar no código e foi `NTEContext` salvo e permanece incorrompido.</span><span class="sxs-lookup"><span data-stu-id="1ebda-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="1ebda-131">Próxima etapa: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="1ebda-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="1ebda-132">Etapa anterior: [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="1ebda-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
