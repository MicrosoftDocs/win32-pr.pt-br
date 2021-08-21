---
description: Objeto de grupo do portal
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objeto de grupo do portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057954"
---
# <a name="portal-group-object"></a>Objeto de grupo do portal

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de grupo de portais modela um grupo de portal iSCSI que está contido em um destino iSCSI.

Use o método [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) para determinar os grupos de portal que estão contidos por um destino específico. Use o método [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) para determinar os grupos de portal que estão associados a um portal especificado. Os chamadores podem obter um ponteiro para um grupo específico do portal selecionando o objeto do grupo do portal desejado da enumeração que é retornada pelo método **QueryPortalGroups** ou o método **QueryAssociatedPortalGroups** . Com um objeto de grupo do portal, você pode adicionar ou remover portais e consultar Propriedades do grupo de portal, portais associados e o destino que contém o grupo do Portal.

As propriedades do objeto do grupo de portais incluem um [identificador de objeto](vds-data-types.md) e a marca do grupo do Portal. Para obter mais informações sobre marcas de grupo do portal, consulte a especificação iSCSI em <https://go.microsoft.com/fwlink/p/?linkid=158752> .

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Enumerações associadas                                                                   | Nenhum.                                                                                                                                              |
| Estruturas associadas                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notificação do grupo de portais do portal de propriedades e do [**portal do VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
