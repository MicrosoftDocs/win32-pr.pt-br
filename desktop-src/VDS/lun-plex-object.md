---
description: Objeto de plex de LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Objeto de plex de LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781530"
---
# <a name="lun-plex-object"></a>Objeto de plex de LUN

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de plex de LUN modela um plex de LUN que está contido por um LUN. Somente um LUN espelhado pode ter vários plexes; todos os outros tipos de LUN têm um plex. Cada plex contém uma cópia dos dados no LUN. Novos plexes podem ser adicionados a um LUN e, com exceção do plex original, os plexes existentes podem ser removidos. O VDS dá suporte a quatro tipos de plex de LUN: simples, estendido, distribuído e distribuído com paridade. Para obter uma descrição de cada um desses tipos de LUN, consulte o [objeto LUN](lun-object.md).

Use o método [**IVdsLun:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para adicionar um plex a um LUN e o método [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para excluir o Plex. Você pode consultar os plexes de LUN invocando o método [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) . Você pode obter um ponteiro para um plex de LUN específico selecionando o objeto de plex desejado da enumeração que é retornada pelo método **QueryPlexes** . Com um objeto de Plex, você pode consultar as extensões de unidade e dicas automágicas e aplicar novas dicas.

Além de um identificador de objeto, um nome e um número de série, as propriedades de objeto de plex de LUN incluem o tipo de Plex, o tamanho, o status, a integridade, o estado de transição e os sinalizadores; uma lista de desmascaramento e tamanho de distribuição; e uma configuração de prioridade de recriação.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Enumerações associadas                           | [**VDS \_ \_ \_ Sinalizador de plex de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ status de plex de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)e [**\_ \_ \_ tipo de plex de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Estruturas associadas                             | [**VDS \_ \_ \_ prop Plex de LUN**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

 
