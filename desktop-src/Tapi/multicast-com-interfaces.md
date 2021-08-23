---
description: As interfaces COM multicast permitem o acesso ao recurso de redes para alocar, renovar e liberar concessões em endereços multicast.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Multicast COM Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c87c231f18904e3b0287095f511cf3c82bfd263e23a9e69dd50c02eb491616d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575536"
---
# <a name="multicast-com-interfaces"></a>Multicast COM Interfaces

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

As interfaces COM multicast permitem o acesso à instalação da rede para alocar, renovar e liberar concessões em endereços multicast. Eles encapsulam um conjunto de definições de estrutura de dados e função. As interfaces COM liberam o programador da carga de compreensão e manipulação dessas estruturas de dados. Além disso, como a TAPI 3 em si é baseada em COM, essas interfaces disponibilizam a alocação de endereços multicast de maneira consistente com os outros recursos fornecidos pela TAPI 3. Aplicativos escritos usando Visual Basic, Java ou linguagens de script que normalmente não podem acessar a API Windows são capazes de usar diretamente essas interfaces.

No momento, a alocação de endereços multicast é o assunto de um grupo de trabalho IETF. Para acessar as informações atuais, consulte "MDHCP" ou "MADCAP" e "Rascunho da Internet" usando qualquer mecanismo de pesquisa da Internet. Além de MADCAP, a arquitetura proposta inclui um protocolo para coordenação de servidor para servidor em um domínio ou AS, bem como um protocolo para coordenação entre domínios. Embora essa arquitetura está evoluindo no momento, o cliente não precisa se preocupar com os detalhes desse esquema.

Atualmente, esse componente dá suporte apenas a endereços IP versão 4.

> [!Note]  
> O protocolo usado para essas interfaces é chamado atualmente de MADCAP. Nas versões anteriores, era conhecido como MDHCP.

 

O objeto multicast é criado chamando **CoCreateInstance** na interface [**IMcastAddressAllocation.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) A interface **IMcastAddressAllocation** expõe o método [**EnumerateScopes,**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) que permite que um aplicativo receba uma lista de todos os escopos de multicast disponíveis.

Depois que um escopo de trabalho for obtido, o [**método RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) será usado para solicitar um endereço multicast do servidor. Se a solicitação for bem-sucedida, [**um ponteiro IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) será retornado. O [**método EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) exposto por essa interface pode ser usado para obter os endereços.

Cada objeto de mídia associado à conferência expõe uma interface [**ITConnection.**](itconnection.md) O [**método ITConnection::SetAddressInfo**](itconnection-setaddressinfo.md) permite a atribuição dos endereços multicast obtidos para a mídia da conferência. O endereço deve ser definido para cada interface **ITConnection** de cada objeto de Mídia associado à conferência.

 

 



