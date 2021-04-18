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
# <a name="retrieving-information-using-gettcpstatistics"></a>Recuperando informações usando GetTcpStatistics

A função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) preenche um ponteiro para uma [**estrutura \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) com informações sobre as estatísticas do protocolo TCP para o computador local.

**Para usar o GetTcpStatistics**

1.  Declare algumas variáveis que são necessárias.

    Declare uma  variável DWORD `dwRetVal` que será usada para verificação de erros de chamadas de função. Declare um ponteiro para uma [**variável \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) chamada *pTCPStats* e aloque memória para a estrutura. Verifique se a memória pode ser alocada.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Chame a função [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) com o parâmetro *pTCPStats* para recuperar estatísticas TCP para IPv4 no computador local. Verifique se há erros e retorne o valor de erro na variável **DWORD** `dwRetVal` . Se ocorrer um erro, a `dwRetVal` variável poderá ser usada para a verificação e o relatório de erros mais extensivos.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Se a chamada tiver sido bem-sucedida, acesse os dados retornados [**no \_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) apontados pelo parâmetro *pTCPStats* .
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Libere a memória alocada para a estrutura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) apontada pelo parâmetro *pTCPStats* . Isso deve ser feito depois que o aplicativo não precisar mais dos dados retornados pelo parâmetro *pTCPStats* .
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Próxima etapa: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)

Etapa anterior: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Código-fonte completo

-   [Código-fonte completo do aplicativo auxiliar de IP](complete-ip-helper-application-source-code.md)

 

 
