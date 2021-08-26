---
title: Gerenciar endereços IP com AddIPAddress, DeleteIPAddress
description: A função AddIPAddress adiciona o endereço IPv4 especificado ao adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e726a2e5785641532abb739d61143f9fabfdd10c38e4b51fcd529f20d92503d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870086"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Gerenciar endereços IP com AddIPAddress, DeleteIPAddress

A [**função AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) adiciona o endereço IPv4 especificado ao adaptador especificado. A [**função DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) exclui o endereço IPv4 especificado do adaptador especificado. Essas funções podem ser usadas para adicionar e excluir endereços IPv4 a um adaptador de rede.

Um endereço IPv4 adicionado pela [**função AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) não é persistente. O endereço IPv4 existe apenas enquanto o objeto do adaptador existir. Reiniciar o computador destrói o endereço IPv4, assim como redefine manualmente a NIC (placa de interface de rede).

Depois [**que AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) for chamado com êxito, o DHCP será desabilitado para o endereço IP que foi adicionado. Portanto, funções como [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que exigem que o DHCP seja habilitado, não estarão funcionais no endereço IP adicionado. A [**função DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) pode ser usada para excluir o endereço IPv4 adicionado.

> [!Note]  
> Políticas de grupo, políticas corporativas e outras restrições na rede podem impedir que essas funções seja realizada com êxito. Verifique se o aplicativo tem as permissões de rede necessárias antes de tentar usar essas funções.

 

**Para usar AddIPAddress**

1.  Declare **variáveis ULONG** `NTEContext` chamadas e , ambas `NTEInstance` inicializadas como zero.
    > [!Note]  
    > A variável é o único parâmetro para a `NTEContext` [**função DeleteIPAddress;**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) para excluir o endereço IP adicionado, deve ser `NTEContext` armazenado e inalterado.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Declare variáveis para as estruturas IPAddr e IPMask chamadas `iaIPAddress` e `iaIPMask` , respectivamente. Esses valores são simplesmente inteiros sem sinal. Inicialize as `iaIPAddress` `iaIPMask` variáveis e usando a [**função de \_ ad adicionar inet.**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Chame a [**função AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar o endereço IPv4. Verifique se há erros e retorne o valor do erro para a **variável DWORD** `dwRetVal` (para uma verificação de erro mais ampla).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > O terceiro parâmetro é o índice do adaptador, que pode ser obtido chamando a [**função GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Supõe-se que a variável retornada por essa função seja chamada `pIPAddrTable` . Para obter ajuda com **a função GetIpAddrTable,** consulte [Gerenciando endereço IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Para usar DeleteIpAddress**

-   Chame a [**função DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) passando a `NTEContext` variável como seu parâmetro. Verifique se há erros e retorne o valor do erro para a **variável DWORD** `dwRetVal` (para uma verificação de erro mais ampla).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Para usar [**DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) deve primeiro ser chamado para obter o handle `NTEContext` . O procedimento anterior presume que **AddIPAddress** já foi chamado em algum lugar no código e foi salvo e `NTEContext` permanece incorrupto.

 

Próxima etapa: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)

Etapa anterior: [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
