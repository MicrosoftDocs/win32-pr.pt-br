---
description: Objeto da unidade
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objeto da unidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169665"
---
# <a name="drive-object"></a>Objeto da unidade

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de unidade modela uma unidade de disco físico que está contida em um subsistema. Cada unidade conecta-se a um barramento, ocupa um slot e contém um conjunto de extensões de unidade. Cada unidade pode contribuir com extensões para qualquer número de LUNs. Uma unidade também pode ser designada como um hot spare.

Use o método [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) para determinar as unidades contidas em um subsistema específico. Os chamadores podem obter um ponteiro para uma unidade específica selecionando o objeto de unidade desejado da enumeração que é retornada pelo método **QueryDrives** ou invocando o método [**IVdsSubSystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) e passando o número de barramento e slot desejado. Com um objeto Drive, você pode definir o status da unidade e a consulta para propriedades da unidade, extensões de unidade associadas e o subsistema que contém a unidade.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto da unidade incluem o status, a integridade e os sinalizadores da unidade; o tamanho em bytes; e um número de barramento e slot.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfaces que podem ser expostas por este objeto     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Enumerações associadas                           | [**VDS \_ \_Sinalizador de unidade**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ status da unidade VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)e [**\_ \_ extensão da unidade VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Estruturas associadas                             | [**VDS \_ GERAR \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) notificação de [**\_ unidade \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)de prop e VDS.                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem:: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
