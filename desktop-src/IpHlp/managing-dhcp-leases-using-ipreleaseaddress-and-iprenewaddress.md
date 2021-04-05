---
title: Gerenciar concessões de DHCP com IpReleaseAddress, IpRenewAddress
description: As funções IpReleaseAddress e IpRenewAddress são usadas para liberar e renovar a concessão de DHCP (protocolo de configuração dinâmica de hosts) atual.
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827049"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Gerenciar concessões de DHCP com IpReleaseAddress, IpRenewAddress

As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) são usadas para liberar e renovar a concessão de DHCP (protocolo de configuração dinâmica de hosts) atual. A função **IpReleaseAddress** libera um endereço IPv4 obtido anteriormente por meio do DHCP. A função **IpRenewAddress** renova uma concessão em um endereço IPv4 obtido anteriormente por meio do DHCP. É comum usar essas duas funções juntas, primeiro liberando a concessão com uma chamada para **IpReleaseAddress** e, em seguida, renovando a concessão com uma chamada para a função **IpRenewAddress** .

Quando um cliente DHCP tiver obtido anteriormente uma concessão DHCP e [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) não for chamado antes da função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , a solicitação do cliente DHCP será enviada ao servidor DHCP que emitiu a concessão de DHCP inicial. Esse servidor DHCP pode não estar disponível ou a solicitação DHCP pode falhar. Quando um host tiver obtido anteriormente uma concessão DHCP e **IpReleaseAddress** for chamado antes da função **IpRenewAddress** , o cliente DHCP primeiro liberará o endereço IP obtido e enviará uma solicitação de cliente DHCP para uma resposta de qualquer servidor DHCP disponível.

> [!Note]  
> As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) exigem que o DHCP esteja habilitado para ser executado corretamente.

 

A função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) usa um ponteiro para uma estrutura de mapa de [**índice de \_ adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) como seu único parâmetro. Para obter esse parâmetro, primeiro chame [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo). Para obter ajuda com a função **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

**Para usar o IpReleaseAddress**

1.  Obtenha um ponteiro para uma estrutura de [**mapa de \_ índice de adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) usando a função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Para obter ajuda com a função GetInterfaceInfo, consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Crie um  objeto DWORD `dwRetVal` (usado para verificação de erro). Supõe-se que a variável retornada por **GetInterfaceInfo** seja chamada `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Se o DHCP estiver habilitado, chame a função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , passando a variável de [**mapa de \_ índice do adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como seu parâmetro. Verifique se há erros gerais e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).
    > [!Note]  
    > A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retorna um parâmetro que pode ser usado para verificar se o DHCP está habilitado antes de chamar essas funções. Para obter ajuda com o **GetAdaptersInfo**, consulte [Gerenciando adaptadores de rede usando o GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> É comum usar essas duas funções juntas, chamar a função [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e, em seguida, chamar a função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando a mesma estrutura que o parâmetro para ambas as funções. O procedimento a seguir pressupõe que as funções não são usadas juntas; no entanto, se as funções forem usadas juntas, pule a etapa 1.

 

**Para usar o IpRenewAddress**

1.  Obtenha um ponteiro para uma estrutura de [**mapa de \_ índice de adaptador \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) usando a função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . (Para obter ajuda com a função **GetInterfaceInfo** , consulte [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)). Declare um  objeto DWORD `dwRetVal` (usado para verificação de erro) se essa variável não tiver sido declarada. Supõe-se que a variável retornada por **GetInterfaceInfo** seja chamada `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Chame a função [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando a variável de mapa de [**\_ \_ índice \_ do adaptador IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` como seu parâmetro. Verifique se há erros gerais e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais abrangente).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Próxima etapa: [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Etapa anterior: [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

 

 



