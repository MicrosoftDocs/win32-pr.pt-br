---
description: A função GetIpStatistics preenche um ponteiro para uma estrutura IPSTATS MIB com informações sobre as estatísticas de IP atuais \_ associadas ao sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recuperando informações usando GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c383c49b316eb48e240a8272957dae8ee3ec1671304df8d466b869b7bf4ec0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050266"
---
# <a name="retrieving-information-using-getipstatistics"></a>Recuperando informações usando GetIpStatistics

A [**função GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) preenche um ponteiro para uma estrutura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) com informações sobre as estatísticas de IP atuais associadas ao sistema.

**Para usar GetIpStatistics**

1.  Declare algumas variáveis necessárias.

    Declare uma **variável DWORD** `dwRetval` que será usada para chamadas de função de verificação de erro. Declare um ponteiro para uma [**variável \_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) chamada *pStats* e aloce memória para a estrutura. Verifique se a memória pode ser alocada.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Chame a [**função GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) com o *parâmetro pStats* para recuperar estatísticas de IP para o computador local. Verifique se há erros e retorne o valor do erro na **variável DWORD** `dwRetval` . Se ocorrer um erro, a variável poderá ser usada para `dwRetval` relatórios e verificação de erros mais extensos.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Se a chamada para [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) tiver sido bem-sucedida, imprima alguns dos dados na estrutura [**\_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) do MIB apontada pelo *parâmetro pStats.*
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Liberar a memória alocada para a [**estrutura \_ MIB IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) apontada pelo *parâmetro pStats.* Isso deve ser feito quando o aplicativo não precisar mais dos dados retornados pelo *parâmetro pStats.*
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Próxima etapa: [recuperando informações usando GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Etapa anterior: [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
