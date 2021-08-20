---
description: Objeto de volume
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Objeto de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87887dae233a47ef168546bb4d0bab93389ab72e0e0617b64ea0c80fbfab0e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125386"
---
# <a name="volume-object"></a>Objeto de volume

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de volume modela uma unidade de armazenamento lógico que é criada por um provedor de software e apresentada ao sistema de arquivos como um disco. Cada volume consiste em pelo menos um plex de volume, que é, por sua vez, composto de extensões de um ou mais discos.

## <a name="volume-types"></a>Tipos de volumes

O VDS dá suporte a cinco tipos de volume: simples, estendido, distribuído, espelhado e distribuído com paridade. Volumes simples, estendidos e distribuídos são não tolerantes a falhas; os volumes espelhados e de paridade são tolerantes a falhas. O restante desta seção descreve cada um dos tipos de volume VDS.

-   Um volume simples é uma parte de um disco físico que funciona como se fosse uma unidade fisicamente separada. Um volume simples pode consistir em uma única região em um disco ou em várias regiões do mesmo disco que estão vinculadas.
-   Um volume estendido combina áreas de espaço não alocado de vários discos em um volume lógico, permitindo que você use com mais eficiência todo o espaço e todas as letras de unidade em um sistema de vários discos.
-   Um volume distribuído é criado pela combinação de áreas de espaço livre em dois ou mais discos em um volume lógico. Os volumes distribuídos usam RAID-0, que distribui dados em vários discos. Os volumes distribuídos não podem ser estendidos ou espelhados e não oferecem tolerância a falhas. Se um dos discos que contêm um volume distribuído falhar, todo o volume falhará. Ao criar volumes distribuídos, é melhor usar discos que sejam do mesmo tamanho, modelo e fabricante.
-   Um volume espelhado é um volume tolerante a falhas que fornece redundância de dados usando duas cópias, ou plexes, do volume para duplicar os dados armazenados no volume. Todos os dados gravados no volume espelhado são gravados em ambos os plexes, que estão localizados em discos físicos separados. Se um dos discos físicos falhar, os dados no disco com falha ficarão indisponíveis, mas o sistema continuará a operar usando o disco não afetado.
-   Uma distribuição com volume de paridade é um volume tolerante a falhas com dados e paridade distribuídos intermitentemente em três ou mais discos físicos. Se uma parte de um disco físico falhar, você poderá recriar os dados que estavam na parte com falha dos dados e da paridade restantes. Esse tipo de volume (também chamado de volume RAID-5) é uma boa solução para redundância de dados em um ambiente de computador no qual a maior parte da atividade consiste na leitura de dados.

### <a name="volume-creation"></a>Criação de volume

Os provedores de software básico e dinâmico dão suporte à criação de volume parcialmente direcionado; um chamador especifica somente os atributos que são de interesse específico e permite que o provedor escolha o restante. o VDS monta automaticamente um volume recém-criado, exceto nas plataformas do Windows server 2003, Edição Enterprise e Windows server 2003, datacenter Edition.

### <a name="working-with-volumes"></a>Trabalhando com volumes

Sempre crie um volume dentro do mesmo pacote que os discos que contribuem com ele. Use o método [**IVdsPack:: createvolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para criar um novo objeto de volume. Você pode determinar os volumes contidos em um pacote específico invocando o método [**QueryVolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) , também exposto por [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack). Um chamador pode obter um ponteiro para um volume específico selecionando o objeto de volume desejado da enumeração que é retornada por **QueryVolumes**. Com um objeto de volume, você pode definir o status; consulta de plexes; estender e reduzir o volume; Adicionar, interromper e remover plexes; e exclua o volume.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto de volume incluem o tipo de volume, o tamanho, o status, a integridade, o estado de transição, os sinalizadores e um tipo de sistema de arquivos recomendado.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* e [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Enumerações associadas                           | [**VDS \_ \_Sinalizador de volume**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag), [**\_ \_ status do volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status), [**\_ \_ tipo de volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)e [**\_ \_ \_ tipo de extensão de disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Estruturas associadas                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) [**\_ \_ Notificação**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)de volume prop e VDS.                                                                                                        |



 

**\* Windows Server 2003:** não há suporte para essas interfaces até Windows Vista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de software](software-provider-objects.md)
</dt> </dl>

 

 
