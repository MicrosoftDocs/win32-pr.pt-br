---
description: A função GetIpStatistics preenche um ponteiro para uma \_ estrutura IPSTATS MIB com informações sobre as estatísticas de IP atuais associadas ao sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recuperando informações usando GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779480"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="6050e-103">Recuperando informações usando GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="6050e-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="6050e-104">A função [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) preenche um ponteiro para uma [**estrutura \_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) com informações sobre as estatísticas de IP atuais associadas ao sistema.</span><span class="sxs-lookup"><span data-stu-id="6050e-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="6050e-105">**Para usar o GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="6050e-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="6050e-106">Declare algumas variáveis que são necessárias.</span><span class="sxs-lookup"><span data-stu-id="6050e-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="6050e-107">Declare uma  variável DWORD `dwRetval` que será usada para verificação de erros de chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="6050e-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="6050e-108">Declare um ponteiro para uma [**variável \_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) chamada *pStats* e aloque memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="6050e-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="6050e-109">Verifique se a memória pode ser alocada.</span><span class="sxs-lookup"><span data-stu-id="6050e-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="6050e-110">Chame a função [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) com o parâmetro *pStats* para recuperar as estatísticas de IP para o computador local.</span><span class="sxs-lookup"><span data-stu-id="6050e-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="6050e-111">Verifique se há erros e retorne o valor de erro na variável **DWORD** `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="6050e-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="6050e-112">Se ocorrer um erro, a `dwRetval` variável poderá ser usada para a verificação e o relatório de erros mais extensivos.</span><span class="sxs-lookup"><span data-stu-id="6050e-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="6050e-113">Se a chamada para [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) tiver sido bem-sucedida, imprima alguns dos dados na estrutura [**\_ IPSTATS do MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) apontada pelo parâmetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="6050e-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="6050e-114">Libere a memória alocada para a estrutura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) apontada pelo parâmetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="6050e-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="6050e-115">Isso deve ser feito depois que o aplicativo não precisar mais dos dados retornados pelo parâmetro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="6050e-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="6050e-116">Próxima etapa: [recuperando informações usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="6050e-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="6050e-117">Etapa anterior: [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="6050e-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
