---
description: As interfaces COM multicast permitem acesso à instalação de redes para alocar, renovar e liberar concessões em endereços multicast.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfaces COM multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646657"
---
# <a name="multicast-com-interfaces"></a>Interfaces COM multicast

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

As interfaces COM multicast permitem acesso à instalação da rede para alocar, renovar e liberar concessões em endereços multicast. Eles encapsulam um conjunto de definições de função e estrutura de dados. As interfaces COM liberam o programador da carga de compreender e manipular essas estruturas de dados. Além disso, como a própria TAPI 3 é baseada em COM, essas interfaces tornam a alocação de endereços Multicast acessível de forma consistente com os outros recursos fornecidos pela TAPI 3. Os aplicativos escritos usando Visual Basic, Java ou linguagens de script que normalmente não podem acessar a API do Windows diretamente são capazes de usar essas interfaces.

A alocação de endereço multicast atualmente é o assunto de um grupo de trabalho da IETF. Para acessar as informações atuais, consulte "MDHCP" ou "MADCAP" e "rascunho da Internet" usando qualquer mecanismo de pesquisa da Internet. Além do MADCAP, a arquitetura proposta inclui um protocolo para a coordenação de servidor para servidor em um domínio ou como, bem como um protocolo para a coordenação entre domínios. Embora essa arquitetura esteja em evolução no momento, o cliente não precisa se preocupar com os detalhes desse esquema.

Esse componente atualmente dá suporte apenas a endereços IP versão 4.

> [!Note]  
> O protocolo usado para essas interfaces atualmente é chamado de MADCAP. Em versões anteriores, era conhecido como MDHCP.

 

O objeto multicast é criado chamando **CoCreateInstance** na interface [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) . A interface **IMcastAddressAllocation** expõe o método [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) , que permite que um aplicativo obtenha uma lista de todos os escopos de multicast disponíveis.

Depois que um escopo de trabalho é obtido, o método [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) é usado para solicitar um endereço de multicast do servidor. Se a solicitação for bem-sucedida, um ponteiro [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) será retornado. O método [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) exposto por essa interface pode ser usado para obter os endereços.

Cada objeto de mídia associado à conferência expõe uma interface [**ITConnection**](itconnection.md) . O método [**ITConnection:: SetAddressInfo**](itconnection-setaddressinfo.md) permite a atribuição dos endereços Multicast obtidos para a mídia da conferência. O endereço deve ser definido para cada interface **ITConnection** de cada objeto de mídia associado à conferência.

 

 



