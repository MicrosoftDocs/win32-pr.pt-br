---
description: Preenche um ponteiro para uma estrutura de informações FIXAs \_ com dados sobre as configurações de rede atuais.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Recuperando informações usando GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169872"
---
# <a name="retrieving-information-using-getnetworkparams"></a>Recuperando informações usando GetNetworkParams

A função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) preenche um ponteiro para uma estrutura de [**\_ informações fixas**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) com dados sobre as configurações de rede atuais.

**Para usar o GetNetworkParams**

1.  Declare um ponteiro para um objeto de [**\_ informações fixo**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) chamado *PFixedInfo* e um objeto **ULONG** chamado *ulOutBufLen*. Essas variáveis são passadas como parâmetros para a função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Além disso, crie uma variável **DWORD** *dwRetVal* (usada para verificação de erro).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Aloque memória para as estruturas.
    > [!Note]  
    > O tamanho de *ulOutBufLen* não é suficiente para manter as informações. Consulte a próxima etapa.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Faça uma chamada inicial para [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) para obter o tamanho necessário para a variável *ulOutBufLen* .
    > [!Note]  
    > Essa função falhará e será usada para garantir que a variável *ulOutBufLen* especifique um tamanho suficiente para manter todos os dados retornados para *pFixedInfo*. Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Faça uma segunda chamada para [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) usando a verificação de erro geral e retornando seu valor para a variável **DWORD** *dwRetVal*; usado para verificação de erros mais avançada.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Se a chamada foi bem-sucedida, acesse os dados da estrutura de dados *pFixedInfo* .
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  Libere qualquer memória alocada para a estrutura *pFixedInfo* .
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Próxima etapa: [Gerenciando adaptadores de rede usando GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

Etapa anterior: [criando um aplicativo auxiliar de IP básico](creating-a-basic-ip-helper-application.md)

 

 



