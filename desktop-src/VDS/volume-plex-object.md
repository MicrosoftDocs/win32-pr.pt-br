---
description: Objeto de plex de volume
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Objeto de plex de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603019"
---
# <a name="volume-plex-object"></a>Objeto de plex de volume

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de volume Plex modela um plex de volume que está contido por um volume. Somente um volume espelhado pode ter vários plexes; todos os outros tipos de volume têm um plex. Cada plex contém uma cópia dos dados no volume. O VDS dá suporte a quatro tipos de plex de volume: simples, estendido, distribuído e distribuído com paridade. Para obter uma descrição de cada um desses tipos de volume, consulte o [objeto volume](volume-object.md).

Há duas maneiras de criar um volume com vários plexes. Você pode usar o método [**IVdsPack:: createvolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para criar o volume espelhado diretamente ou usar o método [**IVdsVolume:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) para adicionar um volume a outro volume. Os volumes (e os discos subjacentes) devem estar no mesmo pacote. A ilustração a seguir mostra um exemplo de como adicionar um volume (B) como um plex a outro volume (A) e o volume multiplexado resultante (A). Os dados no volume A permanecem intactos, enquanto os dados no volume B se tornam uma cópia espelhada dos dados no volume A.

![Diagrama que mostra dois plexes únicos, um com volume simples A e um com volume simples B, igual a vários plexes com volume espelhado A.](images/vdsplex.png)

Você pode consultar os plexes de volume invocando o método [**IVdsVolume:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) . Você pode obter um ponteiro para um plex de volume específico selecionando o objeto de plex desejado da enumeração que é retornada por **QueryPlexes**. Com exceção do último Plex, os plexes existentes podem ser desfeitos ou removidos. Use o [**IVdsVolume:: BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) para dividir um plex de um volume e converter o objeto de plex quebrado em um objeto de volume. Use [**IVdsVolume:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) para excluir o Plex completamente. Você pode tentar reparar um plex tolerante a falhas chamando o método [**IVdsVolumePlex:: Repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) , que move Membros inválidos para bons discos.

Além de um identificador de objeto e tipo de Plex, as propriedades de objeto de plex de volume incluem o status, a integridade e o estado de transição do plex. Este objeto não tem nenhum sinalizador.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Digite                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Enumerações associadas                           | [**VDS \_ \_ \_ Status de plex de volume**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**\_ \_ \_ tipo de plex de volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)e [**\_ \_ \_ tipo de extensão de disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Estruturas associadas                             | [**VDS \_ \_ \_ prop de plex de volume**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto de volume](volume-object.md)
</dt> </dl>

 

 
