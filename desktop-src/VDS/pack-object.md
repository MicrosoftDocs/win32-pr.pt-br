---
description: Objeto Pack
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Objeto Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8c565c45b802258b9d8b9955a2d28adc13c73c989805ce6b2663bc3006d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058015"
---
# <a name="pack-object"></a>Objeto Pack

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de pacote modela um grupo de discos, uma coleção de discos e volumes gerenciados pelo provedor de software básico ou dinâmico. Um provedor pode conter vários objetos de pacote.

Usando a API, os aplicativos podem direcionar o VDS para adicionar um ou mais discos a um pacote, associar os discos a volumes e, opcionalmente, mover os discos como uma unidade entre os hosts. Não é possível importar um volume existente para um pacote.

> [!Note]  
> A associação em um pacote não implica a consistência entre discos em relação ao desempenho, à mídia, ao protocolo de interconexão ou a outras características.

 

Os objetos de disco são não alocados e gerenciados pelo VDS ou são membros de exatamente um pacote. O provedor de software básico pode ter zero ou mais pacotes, cada um contendo um único disco básico. O provedor impõe nenhum limite para o número de volumes em um disco básico. O provedor dinâmico pode ter zero ou mais pacotes com vários discos dinâmicos em cada pacote. Esse provedor limita o número de volumes em um disco, com base no tamanho de um megabyte do banco de dados LDM (Gerenciador de discos lógicos). Considerando que um volume tem pelo menos um plex e uma extensão de disco, o número máximo de volumes para um pacote é de aproximadamente 1000. O número máximo fica inativo conforme o número de discos aumenta.

Além dos objetos de disco, um pacote pode conter um ou mais objetos de LUN implementados por um ou mais provedores de hardware. para o kernel Windows, um LUN é apenas outro disco. (Os objetos de LUN devem ser desmascarados para o computador que está executando o programa do provedor.) Quando o disco é um LUN, o objeto LUN expõe as interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) . Um objeto de pacote usa **IVdsDisk**, em vez de **IVdsLun**, para enumerar os LUNs em um pacote. Para obter uma descrição mais detalhada de um LUN, consulte o [objeto LUN](lun-object.md).

A ilustração a seguir mostra um pacote com dois membros: um disco e um LUN. Um aplicativo pode adicionar esses objetos a um pacote online e criar um volume a partir do disco subjacente e das extensões de unidade representadas por eixos.

![Diagrama que mostra um "pacote" com um disco e um LUN que estão sendo adicionados por um aplicativo para criar um volume representado por uma "unidade" e "eixo".](images/vdsdisksareluns.png)

Use o método [**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um novo objeto de pacote. Os chamadores podem obter um ponteiro para um pacote específico selecionando o objeto de pacote desejado da enumeração que é retornada pelo método [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) . Com um objeto Pack, você pode adicionar, remover ou substituir os membros de um pacote. Quando você adiciona um objeto de disco a um pacote, o VDS Inicializa um disco para desassociar todos os volumes existentes. Por outro lado, um LUN retém todos os detalhes de ligação quando ele é adicionado a um pacote. Se você remover o último disco de um pacote, o VDS excluirá o objeto Pack quando o chamador liberar a última referência ao objeto.

As propriedades do objeto incluem um identificador de objeto, um nome, um status do pacote e sinalizadores. Um pacote online está disponível para configuração e uso, um pacote offline está indisponível. O VDS dá suporte a qualquer número de pacotes online e offline.

**Windows Server 2003:** Dá suporte a apenas um pacote online por vez.

O VDS impõe um quorum de discos online dentro de um pacote. O quorum determina se um pacote pode ter um status online e impede que vários hosts conceda um status online ao mesmo pacote. Se o número de discos online em um pacote cair abaixo do quorum (n/2 + 1), o VDS coloca o pacote online offline.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) e [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Enumerações associadas                           | [**VDS \_ \_Sinalizador de pacote**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) e [**\_ \_ status do VDS Pack**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Estruturas associadas                             | [**VDS \_ Notificação do pacote \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) e do [**VDS \_ Pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003:** essa interface não tem suporte até Windows Vista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
