---
description: A função GetIpAddrTable preenche um ponteiro para uma estrutura IPADDRTABLE MIB com informações sobre os endereços IP atuais \_ associados ao sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gerenciando endereços IP usando GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090bdb1e73d3f770eafb3a5e70893253918eb68573ebd05aa6ec40a609a7ba4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146679"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Gerenciando endereços IP usando GetIpAddrTable

A [**função GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) preenche um ponteiro para uma estrutura [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) com informações sobre os endereços IP atuais associados ao sistema.

**Para usar GetIpAddrTable**

1.  Declare um ponteiro para um [**objeto \_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) chamado *pIPAddrTable* e um **objeto DWORD** chamado *dwSize*. Essas variáveis são passadas como parâmetros para a [**função GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Crie também uma **variável DWORD** chamada *dwRetVal* (usada para verificação de erros).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Alocar memória para a estrutura.
    > [!Note]  
    > O tamanho de *dwSize* não é suficiente para manter as informações. Consulte a próxima etapa.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Faça uma chamada inicial para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) para obter o tamanho necessário para a *variável dwSize.*
    > [!Note]  
    > Essa chamada para a função deve falhar e é usada para garantir que a variável *dwSize* especifique um tamanho suficiente para manter todas as informações retornadas para *pIPAddrTable.* Esse é um modelo de programação comum para estruturas de dados e funções desse tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Faça uma segunda chamada para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) com verificação de erro geral e retorne seu valor para a variável **DWORD** *dwRetVal* (para verificação de erro mais avançada).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Se a chamada foi bem-sucedida, acesse os dados da estrutura *de dados pIPAddrTable.*
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Liberar qualquer memória alocada para a estrutura *pIPAddrTable.*
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Os **objetos DWORD** *dwAddr* e *dwMask* são retornados como valores numéricos na ordem de byte do host, não na ordem de byte de rede. Esses valores não são endereços IP pontilhados.

 

Próxima etapa: [gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Etapa anterior: [gerenciando interfaces usando GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
