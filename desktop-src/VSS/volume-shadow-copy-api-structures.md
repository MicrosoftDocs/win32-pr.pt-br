---
description: As estruturas a seguir são definidas na API de cópia de sombra de volume.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Estruturas de API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590548"
---
# <a name="volume-shadow-copy-api-structures"></a>Estruturas de API de cópia de sombra de volume

As estruturas a seguir são definidas na API de cópia de sombra de volume.



| Estrutura                                                           | Descrição                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contém informações sobre um determinado componente.                                                                                                                                                                                                                       |
| [**\_prop da \_ área de comparação do VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Descreve as associações entre os volumes de origem que contêm os dados de arquivo original e os volumes que contêm a área de armazenamento de cópia de sombra.                                                                                                                                |
| [**\_prop do \_ volume \_ diff do VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Descreve um volume de área de armazenamento de cópia de sombra.                                                                                                                                                                                                                        |
| [**\_prop do \_ objeto de gerenciamento do VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Descreve as propriedades de um volume, volume de armazenamento de cópia de sombra ou uma área de armazenamento de cópia de sombra.                                                                                                                                                                    |
| [**\_União de \_ objeto de gerenciamento do VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Uma União do [**VSS \_ volume \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), do [**VSS \_ diff \_ volume \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)e das estruturas [**\_ \_ \_ prop da área de comparação do VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) usadas pela estrutura de [**\_ \_ \_ prop do objeto de gerenciamento do VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_objeto VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Descreve as propriedades de um provedor, volume, cópia de sombra ou conjunto de cópias de sombra.                                                                                                                                                                                    |
| [**\_União de objeto VSS \_**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Uma União de estruturas de prop do [**VSS \_ \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) e do [**\_ provedor \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) , usada pela estrutura de [**prop do \_ objeto \_ do VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) .                                                                    |
| [**\_prop do provedor de VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Especifica as propriedades do provedor de cópia de sombra.                                                                                                                                                                                                                          |
| [**\_prop de instantâneo do VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contém as propriedades de uma cópia de sombra ou conjunto de cópias de sombra.                                                                                                                                                                                                        |
| [**\_prop volume de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Descreve as propriedades de um volume de origem de cópia de sombra.                                                                                                                                                                                                            |
| [**\_informações de \_ proteção de volume do VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contém informações sobre o nível de proteção de cópia de sombra do volume.                                                                                                                                                                                                 |



 

 

 



