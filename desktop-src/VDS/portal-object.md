---
description: Objeto do portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Objeto do portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864516"
---
# <a name="portal-object"></a>Objeto do portal

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto do portal modela um portal iSCSI que está contido em um subsistema iSCSI.

Use o método [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) para determinar os portais iSCSI do subsistema. Os chamadores podem obter um ponteiro para um portal específico selecionando o objeto do portal desejado da enumeração que é retornada pelo método **QueryPortals** . Com um objeto do portal, você pode definir o status e a consulta do portal para propriedades do portal, grupos de portais associados e o subsistema que contém o Portal.

Um objeto do portal só pode ser associado a no máximo um grupo de portal de um destino especificado.

Os portais servem como um dos pontos de extremidade dos caminhos do MPIO em provedores de hardware iSCSI, nos quais as políticas de balanceamento de carga podem ser impostas.

As propriedades do objeto do portal incluem um identificador de objeto, um endereço IP e uma porta e o status do Portal.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Enumerações associadas                                                                   | [**VDS \_ \_ \_ status do portal iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Estruturas associadas                                                                     | [**VDS \_ Notificação do portal do ISCSI \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) e da [**\_ porta \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
