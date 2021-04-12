---
description: O IOCTL de classificação da lista de endereços do SIO \_ \_ \_ permite que os desenvolvedores de aplicativos classifiquem uma lista de endereços de destino IPv6 e IPv4 para determinar o melhor endereço disponível para fazer uma conexão. O \_ IOCTL de classificação da lista de endereços sio \_ \_ tem suporte no Windows XP e versões posteriores.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Usando SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171467"
---
# <a name="using-sio_address_list_sort"></a>Usando a \_ \_ classificação da lista de endereços do sio \_

O IOCTL de classificação da lista de endereços do sio permite que os desenvolvedores de aplicativos classifiquem uma lista de endereços de destino IPv6 e IPv4 para determinar o melhor endereço disponível para fazer uma conexão. **\_ \_ \_** O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** tem suporte no Windows XP e versões posteriores.

No Windows Vista e posterior, a função [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) usa uma lista fornecida de possíveis endereços IP de destino, emparelha os endereços de destino com os endereços IP locais da máquina host e classifica os pares de acordo com o qual o par de endereços é mais adequado para a comunicação entre os dois pares. A função **CreateSortedAddressPairs** deve ser usada em vez do IOCTL de classificação da lista de endereços do **sio \_ \_ \_** no Windows Vista e posterior.

As seções a seguir descrevem as considerações de uso para a **classificação da lista de endereços do sio \_ \_ \_**.

## <a name="parameters"></a>Parâmetros

O buffer passado para **a \_ \_ \_ classificação da lista de endereços sio** é uma estrutura de [**\_ \_ lista de endereços de soquete**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) . Cada [**\_ endereço de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) na lista deve estar no \_ formato SOCKADDR In6.

O IOCTL de classificação da lista de endereços do sio classifica os endereços IPv6 e IPv4 no Windows Vista e versões posteriores. **\_ \_ \_** Todos os endereços IPv4 na lista a serem classificados devem estar no formato de endereço IPv6 mapeado para IPv4. Para obter mais informações sobre o formato de endereço IPv6 mapeado para IPv4, consulte [soquetes de pilha dupla](dual-stack-sockets.md).

No Windows Server 2003 e no Windows XP, **a \_ \_ \_ classificação da lista de endereços do sio** classifica somente endereços IPv6. Não há suporte para endereços IPv4 no formato de endereço IPv6 mapeados para IPv4.

Na saída, o membro **iAddressCount** da estrutura [**da \_ \_ lista de endereços de soquete**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) pode ser menor do que na entrada se o código do IOCTL determinar que alguns endereços de destino são inválidos.

## <a name="sorting-determination"></a>Determinação da classificação

A ordem de classificação para endereços IPv6 para a lista de endereços do SIO de \_ \_ classificação do \_ IOCTL é baseada na tabela de política de prefixo. A tabela de diretivas de prefixo é configurada usando o utilitário de linha de comando *Netsh.exe* . Os trechos de linha de comando a seguir ilustram os comandos básicos de configuração de tabela de prefixo de *Netsh.exe* :

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> No Windows Server 2003 e no Windows XP, o primeiro comando netsh listado acima foi o seguinte. Todos os outros comandos relacionados são os mesmos.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

A ordenação de endereço também é determinada por um algoritmo descrito no RFC 3484 na *seleção de endereço padrão para o IPv6 (protocolo IP versão 6)* publicado pela IETF. Para obter mais informações, confira [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Este recurso só pode estar disponível em inglês.)

O **IOCTL \_ \_ \_ classificação da lista de endereços do sio** classifica os endereços do melhor para o pior e preenche os membros da **\_ \_ ID de escopo do sin6** , se necessário. Para endereços de site local, a lista de endereços SIOs é \_ \_ \_ preenchida ou elimina o endereço de escopo.

O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** ignora o endereço de origem associado ao soquete e classifica apenas pela lista de endereços de destino passada como um parâmetro.

A função [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) deve ser usada em vez do IOCTL de classificação da lista de endereços do **sio \_ \_ \_** no Windows Vista e posterior. A função **CreateSortedAddressPairs** retorna uma lista de pares de endereços que contém um endereço de origem local e um endereço de destino. Isso fornece um aplicativo o endereço de origem correto a ser usado para cada endereço de destino. Um aplicativo também pode filtrar os resultados procurando por um endereço de origem específico. nos resultados.

## <a name="requirements"></a>Requisitos

O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** é definido no arquivo de cabeçalho *Winsock2. h* . No SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o **sio de classificação da \_ \_ lista \_ de endereços** é definido no arquivo de cabeçalho *Ws2def. h* . Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

O IOCTL de **\_ classificação da \_ lista \_ de endereços sio** tem suporte no Windows XP e versões posteriores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
