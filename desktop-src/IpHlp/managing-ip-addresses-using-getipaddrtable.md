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
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Gerenciando endereços IP usando GetIpAddrTable

A função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) preenche um ponteiro para uma [**estrutura \_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) com informações sobre os endereços IP atuais associados ao sistema.

**Para usar o GetIpAddrTable**

1.  Declare um ponteiro para um [**objeto \_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) chamado *PIPAddrTable* e um objeto **DWORD** chamado *dwSize*. Essas variáveis são passadas como parâmetros para a função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Além disso, crie uma variável **DWORD** chamada *dwRetVal* (usada para verificação de erro).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Aloque memória para a estrutura.
    > [!Note]  
    > O tamanho de *dwSize* não é suficiente para manter as informações. Consulte a próxima etapa.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Faça uma chamada inicial para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) para obter o tamanho necessário na variável *dwSize* .
    > [!Note]  
    > Essa chamada para a função é destinada a falhar e é usada para garantir que a variável *dwSize* especifique um tamanho suficiente para manter todas as informações retornadas para *pIPAddrTable*. Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Faça uma segunda chamada para [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) com verificação de erro geral e retorne seu valor para a variável **DWORD** *dwRetVal* (para verificação de erros mais avançada).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Se a chamada foi bem-sucedida, acesse os dados da estrutura de dados *pIPAddrTable* .
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Libere qualquer memória alocada para a estrutura *pIPAddrTable* .
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Os  objetos DWORD *dwAddr* e *dwMask* são retornados como valores numéricos na ordem de bytes do host, não na ordem de bytes de rede. Esses valores não são endereços IP pontilhados.

 

Próxima etapa: [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Etapa anterior: [Gerenciando interfaces usando GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
