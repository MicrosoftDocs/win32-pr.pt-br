---
title: Gerenciar endereços IP com AddIPAddress, DeleteIPAddress
description: A função AddIPAddress adiciona o endereço IPv4 especificado ao adaptador especificado.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779914"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Gerenciar endereços IP com AddIPAddress, DeleteIPAddress

A função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) adiciona o endereço IPv4 especificado ao adaptador especificado. A função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) exclui o endereço IPv4 especificado do adaptador especificado. Essas funções podem ser usadas para adicionar e excluir endereços IPv4 para um adaptador de rede.

Um endereço IPv4 adicionado pela função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) não é persistente. O endereço IPv4 existe somente contanto que o objeto adaptador exista. A reinicialização do computador destrói o endereço IPv4, assim como a redefinição manual da NIC (placa de interface de rede).

Após a chamada de [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) com êxito, o DHCP será desabilitado para o endereço IP que foi adicionado. Portanto, funções como [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), que exigem DHCP para serem habilitadas, não estarão funcionais no endereço IP adicionado. A função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) pode ser usada para excluir o endereço IPv4 adicionado.

> [!Note]  
> As políticas de grupo, as políticas corporativas e outras restrições na rede podem impedir que essas funções sejam concluídas com êxito. Verifique se o aplicativo tem as permissões de rede necessárias antes de tentar usar essas funções.

 

**Para usar o AddIPAddress**

1.  Declare as variáveis **ULONG** chamadas `NTEContext` e `NTEInstance` , ambas inicializadas como zero.
    > [!Note]  
    > A `NTEContext` variável é o único parâmetro para a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) ; para excluir o endereço IP que é adicionado, `NTEContext` deve ser armazenado e inalterado.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Declare variáveis para as estruturas IPAddr e IPMask chamadas `iaIPAddress` e `iaIPMask` , respectivamente. Esses valores são simplesmente números inteiros sem sinal. Inicialize as `iaIPAddress` `iaIPMask` variáveis e usando a função de [**\_ endereço inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Chame a função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar o endereço IPv4. Verifique se há erros e retorne o valor de erro para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > O terceiro parâmetro é o índice do adaptador, que pode ser obtido chamando-se a função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Supõe-se que a variável retornada por essa função é nomeada `pIPAddrTable` . Para obter ajuda com a função **GetIpAddrTable** , consulte [Gerenciando o endereço IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Para usar o DeleteIpAddress**

-   Chame a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , passando a `NTEContext` variável como seu parâmetro. Verifique se há erros e retorne o valor de erro para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Para usar [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) deve primeiro ser chamado para obter o identificador `NTEContext` . O procedimento anterior pressupõe que **AddIPAddress** já foi chamado em algum lugar no código e foi `NTEContext` salvo e permanece incorrompido.

 

Próxima etapa: [recuperando informações usando GetIpStatistics](retrieving-information-using-getipstatistics.md)

Etapa anterior: [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
