---
description: Objeto LUN Plex
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Objeto LUN Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df52b60bcbd23269d766435749b40b8c636361390359182a38a695ab6252a27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999436"
---
# <a name="lun-plex-object"></a>Objeto LUN Plex

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto lun plex modela um plex lun contido por um LUN. Somente um LUN espelhado pode ter vários plexes; todos os outros tipos de LUN têm um plex. Cada plex contém uma cópia dos dados no LUN. Novos plexes podem ser adicionados a um LUN e, com exceção do plex original, os plexes existentes podem ser removidos. O VDS dá suporte a quatro tipos de LUN plex: simples, ampliado, com faixa e sem paridade. Para ver uma descrição de cada um desses tipos de LUN, consulte o Objeto [LUN](lun-object.md).

Use o [**método IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para adicionar um plex a um LUN e o método [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para excluir o plex. Você pode consultar os plexes de LUN invocando o [**método IVdsLun::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) Você pode obter um ponteiro para um plex de LUN específico selecionando o objeto plex desejado na enumeração que é retornada pelo **método QueryPlexes.** Com um objeto plex, você pode consultar as extensão de unidade e dicas de automação e aplicar novas dicas.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto lun plex incluem o tipo de plex, o tamanho, o status, a saúde, o estado de transição e os sinalizadores; uma lista de máscaras e tamanho de faixa; e uma configuração de prioridade de recomposição.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsLunPlex.**](/windows/desktop/api/Vds/nn-vds-ivdslunplex)                                                                                                                              |
| Enumerações associadas                           | [**VDS \_ SINALIZADOR \_ LUN \_ PLEX,**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag) [**STATUS DO LUN DO VDS \_ \_ E \_**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)TIPO [**\_ \_ PLEX \_ DO LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Estruturas associadas                             | [**VDS \_ PROP \_ DO \_ LUN PLEX.**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop)                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

 
