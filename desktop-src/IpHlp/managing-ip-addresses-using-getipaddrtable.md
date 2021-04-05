---
description: A função GetIpAddrTable preenche um ponteiro para uma \_ estrutura IPADDRTABLE MIB com informações sobre os endereços IP atuais associados ao sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gerenciando endereços IP usando GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828267"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="3126d-103">Gerenciando endereços IP usando GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="3126d-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="3126d-104">A função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) preenche um ponteiro para uma [**estrutura \_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) com informações sobre os endereços IP atuais associados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="3126d-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="3126d-105">**Para usar o GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="3126d-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="3126d-106">Declare um ponteiro para um [**objeto \_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) chamado *PIPAddrTable* e um objeto **DWORD** chamado *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="3126d-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="3126d-107">Essas variáveis são passadas como parâmetros para a função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="3126d-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="3126d-108">Além disso, crie uma variável **DWORD** chamada *dwRetVal* (usada para verificação de erro).</span><span class="sxs-lookup"><span data-stu-id="3126d-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="3126d-109">Aloque memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="3126d-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="3126d-110">O tamanho de *dwSize* não é suficiente para manter as informações.</span><span class="sxs-lookup"><span data-stu-id="3126d-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="3126d-111">Consulte a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="3126d-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="3126d-112">Faça uma chamada inicial para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) para obter o tamanho necessário na variável *dwSize* .</span><span class="sxs-lookup"><span data-stu-id="3126d-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="3126d-113">Essa chamada para a função é destinada a falhar e é usada para garantir que a variável *dwSize* especifique um tamanho suficiente para manter todas as informações retornadas para *pIPAddrTable*.</span><span class="sxs-lookup"><span data-stu-id="3126d-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="3126d-114">Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.</span><span class="sxs-lookup"><span data-stu-id="3126d-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="3126d-115">Faça uma segunda chamada para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) com verificação de erro geral e retorne seu valor para a variável **DWORD** *dwRetVal* (para verificação de erros mais avançada).</span><span class="sxs-lookup"><span data-stu-id="3126d-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="3126d-116">Se a chamada foi bem-sucedida, acesse os dados da estrutura de dados *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="3126d-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="3126d-117">Libere qualquer memória alocada para a estrutura *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="3126d-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="3126d-118">Os  objetos DWORD *dwAddr* e *dwMask* são retornados como valores numéricos na ordem de bytes do host, não na ordem de bytes de rede.</span><span class="sxs-lookup"><span data-stu-id="3126d-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="3126d-119">Esses valores não são endereços IP pontilhados.</span><span class="sxs-lookup"><span data-stu-id="3126d-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="3126d-120">Próxima etapa: [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="3126d-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="3126d-121">Etapa anterior: [Gerenciando interfaces usando GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="3126d-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
