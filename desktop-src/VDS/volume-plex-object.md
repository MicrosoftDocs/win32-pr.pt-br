---
description: Objeto Volume Plex
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Objeto Volume Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603019"
---
# <a name="volume-plex-object"></a>Objeto Volume Plex

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto plex de volume modela um volume plex contido por um volume. Somente um volume espelhado pode ter vários plexes; todos os outros tipos de volume têm um plex. Cada plex contém uma cópia dos dados no volume. O VDS dá suporte a quatro tipos de volume plex: simples, ampliado, em faixa e em faixa com paridade. Para uma descrição de cada um desses tipos de volume, consulte o [Objeto de Volume](volume-object.md).

Há duas maneiras de criar um volume com vários plexes. Você pode usar o método [**IVdsPack::CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) para criar o volume espelhado diretamente ou usar o método [**IVdsVolume::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) para adicionar um volume a outro volume. Os volumes (e os discos subjacentes) devem estar no mesmo pacote. A ilustração a seguir mostra um exemplo de como adicionar um volume (B) como um plex a outro volume (A) e o volume multiplexado resultante (A). Os dados no volume A permanecem intactos, enquanto os dados no volume B se tornam uma cópia espelhada dos dados no volume A.

![Diagrama que mostra dois simples plexes, um com o volume A simples e outro com o volume B simples, igual a vários plexes com o volume espelhado A.](images/vdsplex.png)

Você pode consultar porplexes de volume invocando o [**método IVdsVolume::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) Você pode obter um ponteiro para um plex de volume específico selecionando o objeto plex desejado na enumeração que é retornada por **QueryPlexes**. Com exceção do último plex, os plexes existentes podem ser desfeitos ou removidos. Use [**o IVdsVolume::BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) para dividir um plex de um volume e converter o objeto plex desfeito em um objeto de volume. Use [**o IVdsVolume::RemovePlex para**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) excluir completamente o plex. Você pode tentar reparar um plex tolerante a falhas chamando o método [**IVdsVolumePlex::Repair,**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) que move membros ruins para discos bons.

Além de um identificador de objeto e tipo de plex, as propriedades do objeto do volume plex incluem o status, a saúde e o estado de transição do plex. Esse objeto não tem sinalizadores.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsVolumePlex.**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex)                                                                                                                                          |
| Enumerações associadas                           | [**VDS \_ STATUS \_ DO \_ VOLUME PLEX,**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status)TIPO PLEX DE [**VOLUME VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)e TIPO DE EXTENSÃO DE DISCO [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Estruturas associadas                             | [**VDS \_ PROP \_ DO \_ VOLUME PLEX.**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop)                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do provedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto Volume](volume-object.md)
</dt> </dl>

 

 
