---
description: O tamanho do pacote de mídia afeta a capacidade dos protocolos IPX de transferir dados entre redes e pode ser desafiador lidar com o de maneira independente de transporte.
ms.assetid: cce31a6a-c187-4ec4-976c-5f9984211ccb
title: Sobre o tamanho do pacote de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03be30402dc94b22315292b281565572f04cbc89803eeed79f67d55a77ceeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412186"
---
# <a name="about-media-packet-size"></a>Sobre o tamanho do pacote de mídia

O tamanho do pacote de mídia afeta a capacidade dos protocolos IPX de transferir dados entre redes e pode ser desafiador lidar com o de maneira independente de transporte. O IPX não segmenta pacotes nem relata quando os pacotes são descartados devido a violações de tamanho. Isso significa que alguma entidade na estação final deve manter o conhecimento do tamanho máximo do pacote a ser usado em qualquer caminho de trabalho na Internet. Tradicionalmente, os datagramas IPX e os serviços orientados à conexão SPX têm deixado essa carga para o aplicativo, enquanto o SPXII usou uma grande negociação de pacotes da Internet para lidar com isso de forma transparente.

O Winsock tenta definir limites de tamanho de pacote racional para seus vários protocolos IPX, conforme descrito na próxima seção. Esses limites podem ser exibidos e modificados por aplicativos por meio de opções de soquete get/set. Ao determinar o tamanho máximo do pacote, as três áreas de interesse são:

-   \# Tamanho do pacote de mídia
-   \# Tamanho do pacote de tabela
-   \# Tamanho do pacote da estação final

*O tamanho do pacote de* mídia reflete o tamanho máximo do pacote aceitável em qualquer mídia que o pacote atravessa para seu destino. O tamanho do pacote varia entre mídias diferentes, como Ethernet e anel de token. A quantidade de espaço de dados dentro de um pacote também pode variar dentro de uma determinada mídia, dependendo da disposição do header do pacote. Por exemplo, o tamanho efetivo dos dados de um pacote Ethernet varia dependendo se ele é do tipo Ethernet II, Ethernet 802.2 ou Ethernet SNAP.

*O tamanho do pacote escalável* reflete o tamanho máximo do pacote que um roteador intermediário está disposto a encaminhar. A maioria dos roteadores IPX é criada para rotear qualquer datagrama de tamanho, desde que ele permaneça dentro do tamanho da mídia da rede de envio e recebimento. No entanto, roteadores mais antigos podem limitar o tamanho máximo do pacote a 576 bytes, incluindo os headers de protocolo.

*O tamanho do pacote da estação* final reflete o tamanho dos buffers de escuta que as estações de extremidade publicaram para receber pacotes de entrada. Mesmo quando os limites de mídia e roteador permitem a passagem de um pacote, ele pode ser descartado pela estação final se o aplicativo receptor tiver postado um buffer menor. Muitos aplicativos IPX/SPX tradicionais limitam o tamanho do buffer de recebimento, de forma que a parte de dados não deve ser maior que 512 ou 1024 bytes.

 

 



