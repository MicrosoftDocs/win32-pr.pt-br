---
description: Um objeto de pool de armazenamento modela um pool de armazenamento em um subsistema de armazenamento.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Objeto do pool de armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810280"
---
# <a name="storage-pool-object"></a>Objeto do pool de armazenamento

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de pool de armazenamento modela um pool de armazenamento em um subsistema de armazenamento.

Um pool de armazenamento contém extensões de unidade de uma ou mais unidades que são gerenciadas pelo mesmo provedor de hardware.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Enumerações associadas                           | [**VDS \_ \_Tipo de RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ status do pool de armazenamento VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)e [**\_ \_ \_ tipo de pool de armazenamento VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Estruturas associadas                             | [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ atributos do pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ atributos personalizados do pool do VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extensão de unidade do pool de armazenamento VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)e [**\_ \_ \_ prop pool de armazenamento do VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
