---
description: A função GetTcpStatistics preenche um ponteiro para uma \_ estrutura TCPSTATS MIB com informações sobre as estatísticas do protocolo TCP para o computador local.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Recuperando informações usando GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780626"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="fe73a-103">Recuperando informações usando GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="fe73a-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="fe73a-104">A função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) preenche um ponteiro para uma [**estrutura \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) com informações sobre as estatísticas do protocolo TCP para o computador local.</span><span class="sxs-lookup"><span data-stu-id="fe73a-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="fe73a-105">**Para usar o GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="fe73a-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="fe73a-106">Declare algumas variáveis que são necessárias.</span><span class="sxs-lookup"><span data-stu-id="fe73a-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="fe73a-107">Declare uma  variável DWORD `dwRetVal` que será usada para verificação de erros de chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="fe73a-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="fe73a-108">Declare um ponteiro para uma [**variável \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) chamada *pTCPStats* e aloque memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="fe73a-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="fe73a-109">Verifique se a memória pode ser alocada.</span><span class="sxs-lookup"><span data-stu-id="fe73a-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="fe73a-110">Chame a função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) com o parâmetro *pTCPStats* para recuperar estatísticas TCP para IPv4 no computador local.</span><span class="sxs-lookup"><span data-stu-id="fe73a-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="fe73a-111">Verifique se há erros e retorne o valor de erro na variável **DWORD** `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="fe73a-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="fe73a-112">Se ocorrer um erro, a `dwRetVal` variável poderá ser usada para a verificação e o relatório de erros mais extensivos.</span><span class="sxs-lookup"><span data-stu-id="fe73a-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="fe73a-113">Se a chamada tiver sido bem-sucedida, acesse os dados retornados [**no \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) apontados pelo parâmetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="fe73a-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="fe73a-114">Libere a memória alocada para a estrutura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) apontada pelo parâmetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="fe73a-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="fe73a-115">Isso deve ser feito depois que o aplicativo não precisar mais dos dados retornados pelo parâmetro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="fe73a-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="fe73a-116">Próxima etapa: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="fe73a-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="fe73a-117">Etapa anterior: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="fe73a-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="fe73a-118">Código-fonte completo</span><span class="sxs-lookup"><span data-stu-id="fe73a-118">Complete Source Code</span></span>

-   [<span data-ttu-id="fe73a-119">Código-fonte completo do aplicativo auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="fe73a-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
