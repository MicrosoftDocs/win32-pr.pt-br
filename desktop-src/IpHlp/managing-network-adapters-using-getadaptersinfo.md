---
description: A função GetAdaptersInfo preenche um ponteiro para uma \_ estrutura de \_ informações do adaptador IP com informações sobre os adaptadores de rede associados ao sistema.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gerenciando adaptadores de rede usando o GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011374"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Gerenciando adaptadores de rede usando o GetAdaptersInfo

A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) preenche um ponteiro para uma estrutura de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) com informações sobre os adaptadores de rede associados ao sistema.

**Para usar o GetAdaptersInfo**

1.  Declare um ponteiro para uma variável de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) chamada *pAdapterInfo* e uma variável **ULONG** chamada *ulOutBufLen*. Essas variáveis são passadas como parâmetros para a função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Além disso, crie uma variável **DWORD** chamada *dwRetVal* (para verificação de erro).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Aloque memória para as estruturas.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Faça uma chamada inicial para [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) para obter o tamanho necessário na variável *ulOutBufLen* .
    > [!Note]  
    > Essa chamada para a função é destinada a falhar e é usada para garantir que a variável *ulOutBufLen* especifique um tamanho suficiente para manter todas as informações retornadas para *pAdapterInfo*. Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Faça uma segunda chamada para [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passando *pAdapterInfo* e *ulOutBufLen* como parâmetros e verificando o erro geral. Retorne seu valor para a variável **DWORD** *dwRetVal* (para verificação de erro mais abrangente).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Se a chamada foi bem-sucedida, acesse alguns dos dados na estrutura *pAdapterInfo* .
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  Libere qualquer memória alocada para a estrutura *pAdapterInfo* .
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Próxima etapa: [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

Etapa anterior: [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 



