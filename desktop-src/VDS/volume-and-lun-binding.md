---
description: Associação de volume e LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Associação de volume e LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172396"
---
# <a name="volume-and-lun-binding"></a>Associação de volume e LUN

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

A associação é a criação de volumes ou LUNs. Os volumes consistem em extensões de disco e LUNs que consistem em extensões de unidade. A associação seleciona um conjunto de mapeamentos para recursos físicos e ocorre dentro de um subsistema, em um pacote ou em ambos. Todos os programas de provedor dão suporte a associação parcialmente direcionada a um modelo no qual o chamador especifica apenas os atributos de associação de interesse específico e permite que o provedor escolha o restante. As operações no VDS para vincular volumes e LUNs são semelhantes, mas não idênticas. Por exemplo, os provedores de hardware podem oferecer opções de associação adicionais.

O VDS dá suporte aos cinco tipos de associação de volume e LUN a seguir para configurações parcialmente direcionadas. (Os provedores de hardware podem e oferecem suporte a muitas outras associações.)



| Termo                                                                                                                                             | Descrição                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Único<br/>                                                     | Mapeamento linear com apenas uma extensão contígua.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Estendidos<br/>                                                 | Mapeamento linear com várias extensões não contíguas em vários discos ou unidades.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Distribuídos<br/>                                                 | Mapeamento que intercala extensões de volume contíguas em vários discos ou unidades.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Espelhado<br/>                                             | Mapeamento que mantém duas ou mais cópias de dados idênticas.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Distribuído com paridade<br/> | Mapeamento que distribui informações de verificação de paridade em vários discos ou unidades.<br/>  |



 

As construções VDS são espelhadas, distribuídas e distribuídas com associações de paridade de mais de um membro. Por exemplo, um espelho bidirecional tem dois membros. Cada membro pode ocupar extensões em mais de um disco ou unidade. O VDS concatena as extensões para formar o membro e, em seguida, associa o volume ou LUN aos membros. Um provedor pode dar suporte A todos os tipos de associação ou qualquer subconjunto. No modelo de objeto do VDS, cada membro de um espelho é um objeto independente chamado de plex.

Novamente, os tipos de volume e LUN são semelhantes, mas não são exatos. Para obter uma descrição dos tipos de volume, consulte o [objeto volume](volume-object.md); para tipos de LUN, consulte o [objeto LUN](lun-object.md). Os tipos de associação são não tolerantes a falhas ou tolerantes a falhas.

### <a name="non-fault-tolerant-binding"></a>Associação não tolerante a falhas

Os volumes não tolerantes a falhas e os LUNs não oferecem recuperação de desastres. Se um dos eixos que contribui para um volume ou LUN tolerante a falhas não falhar, todo o volume ou LUN falhará. No Exchange para o risco de dados, os volumes tolerantes a falhas e LUNs oferecem desempenho de entrada/saída que geralmente é superior ao dos volumes tolerantes a falhas e LUNs. O VDS dá suporte aos três tipos de não-tolerância a falhas a seguir: simples, estendido e distribuído.

Simples

![Diagrama que mostra um tipo simples tolerante a falhas com 2 pacotes e 2 subsistemas.](images/vdssimplelunvol.png)

Estendido

![Diagrama que mostra um tipo de tolerância a falhas não com falha estendida com 1 pacote e 1 subsistema.](images/vdsspanlunvol.png)

Distribuídos

![Diagrama que mostra um tipo não tolerante a falhas distribuído com 1 pacote e 1 subsistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Associação tolerante a falhas

Os seguintes volumes tolerantes a falhas e LUNs oferecem recuperação de desastre. Se um dos eixos que contribuem para um volume tolerante a falhas ou LUN falhar, os dados poderão ser recuperados. No Exchange para segurança de dados, o desempenho de entrada/saída de volumes tolerantes a falhas e LUNs é geralmente inferior ao de volumes tolerantes a falhas e LUNs. O VDS dá suporte a dois tipos de tolerância a falhas: espelhado e distribuído com paridade.

Espelhado (espelho de três vias)

![Diagrama que mostra um tipo de tolerância a falhas de falha (espelho de 3 vias) espelhado.](images/vdsmirrorlunvol.png)

Distribuído com paridade

![Diagrama que mostra uma faixa com tipo tolerante a falhas de paridade.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da configuração](configuration.md)
</dt> <dt>

[Objeto de volume](volume-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

