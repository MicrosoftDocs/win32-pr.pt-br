---
description: As enumerações a seguir são definidas na API de cópia de sombra de volume.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Enumerações de API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813413"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Enumerações de API de cópia de sombra de volume

As enumerações a seguir são definidas na API de cópia de sombra de volume.



| Nome                                                                           | Descrição                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_estado do \_ gravador \_ alternativo do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Define o conjunto de Estados válidos usados para indicar se um gravador tem um gravador alternativo associado.                                                              |
| [**\_nível do aplicativo VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Define o conjunto de níveis de aplicativos válidos.                                                                                                                       |
| [**\_esquema de backup do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Define o conjunto de esquemas de backup — operações com as quais um gravador pode participar.                                                                                          |
| [**\_tipo de backup do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Define o conjunto de tipos de backup.                                                                                                                                   |
| [**\_sinalizadores de componente do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Indica suporte para recuperação automática.                                                                                                                               |
| [**\_tipo de componente do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Define o conjunto de tipos de componentes.                                                                                                                                |
| [**\_status de \_ restauração do arquivo VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Define o conjunto de status de uma operação de restauração de arquivo.                                                                                                           |
| [**\_tipo de \_ backup de especificação do arquivo VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Define o conjunto de operações de backup com suporte dos gravadores.                                                                                                         |
| [**\_\_Opções de hardware do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Define os sinalizadores de LUN de cópia de sombra.                                                                                                                                     |
| [**\_tipo de \_ objeto de gerenciamento do VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminante para a União de União de objeto de gerenciamento do VSS dentro da estrutura de [**prop do objeto de gerenciamento do VSS \_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . [**\_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) |
| [**\_tipo de objeto VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Usado para identificar um objeto como um conjunto de cópias de sombra, uma cópia de sombra ou um provedor.                                                                                         |
| [**\_falha na proteção VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Define o conjunto de falhas de proteção de cópia de sombra.                                                                                                                  |
| [**\_nível de proteção VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Define o conjunto de níveis de proteção de cópias de sombra de volume.                                                                                                           |
| [**\_recursos do provedor do VSS \_**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Reservado para uso futuro.                                                                                                                                           |
| [**\_tipo de provedor VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Define o conjunto de tipos de provedor.                                                                                                                                 |
| [**\_Opções de recuperação do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Usado por um solicitante para especificar como uma operação de ressincronização deve ser executada.                                                                               |
| [**\_destino de restauração do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Define o conjunto de destinos de restauração.                                                                                                                                |
| [**\_tipo de restauração VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Define o conjunto de operações de restauração a serem executadas.                                                                                                              |
| [**\_Enumeração RESTOREMETHOD do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Define o conjunto de métodos de restauração de arquivo padrão para um gravador.                                                                                                      |
| [**\_tipo de avanço VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Usado por um solicitante para indicar o tipo de operação de roll-forward que está prestes a executar.                                                                         |
| [**\_compatibilidade de instantâneo do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Define o conjunto de operações de controle de volume ou de e/s de arquivo que podem ser desabilitadas para um volume que foi copiado por sombra.                                            |
| [**\_\_contexto de instantâneo do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Especifica como uma cópia de sombra deve ser criada, consultada ou excluída e o grau de envolvimento do gravador.                                                            |
| [**\_estado do instantâneo do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Define o conjunto de Estados de uma operação de cópia de sombra.                                                                                                              |
| [**\_tipo de origem do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Define o conjunto de tipos de dados que um gravador pode gerenciar.                                                                                                         |
| [**\_máscara de assinatura do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Define o conjunto de eventos que um gravador pode receber.                                                                                                               |
| [**\_tipo de uso do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Especifica como o sistema host usa os dados gerenciados por um gravador.                                                                                                   |
| [**\_\_atributos de \_ instantâneo de volume do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Define o conjunto de atributos de uma cópia de sombra.                                                                                                                    |
| [**\_estado do gravador VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Define o conjunto de Estados do gravador.                                                                                                                           |
| [**\_Enumeração WRITERRESTORE do VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Define o conjunto de condições sob as quais um gravador manipulará eventos gerados durante uma operação de restauração.                                                        |



 

 

 



