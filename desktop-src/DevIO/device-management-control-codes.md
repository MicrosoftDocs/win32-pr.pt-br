---
description: Os códigos de controle a seguir são usados com os dispositivos de trocador.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Códigos de controle de gerenciamento de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010246"
---
# <a name="device-management-control-codes"></a>Códigos de controle de gerenciamento de dispositivos

Os códigos de controle a seguir são usados com os dispositivos de trocador.



| Valor                                                                                          | Significado                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**intercâmbio de trocador de IOCTL \_ \_ \_ médio**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Move uma parte da mídia de um elemento de origem para um destino e a parte da mídia originalmente no primeiro destino para um segundo destino. |
| [**\_status do \_ \_ elemento Get do ALTERADOr de IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Recupera o status de todos os elementos ou um número especificado de elementos de um tipo específico.                                                         |
| [**\_parâmetros Get do alterador de IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Recupera os parâmetros do dispositivo especificado.                                                                                                    |
| [**\_trocador de IOCTL \_ obter \_ dados do produto \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Recupera os dados do produto para o dispositivo especificado.                                                                                                 |
| [**\_status de obtenção do alterador de IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Recupera o status atual do dispositivo especificado.                                                                                                |
| [**\_status do \_ elemento de inicialização do alterador de \_ IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Inicializa o status de todos os elementos ou dos elementos especificados de um tipo específico.                                                               |
| [**\_movimentação de trocador de IOCTL \_ \_ média**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Move uma parte da mídia para um destino.                                                                                                             |
| [**\_marcas de \_ volume de consulta do alterador de \_ IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Recupera as informações de marca de volume para os elementos especificados.                                                                                     |
| [**o \_ alterador de IOCTL \_ reinicializa o \_ transporte**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Recalibrar fisicamente um elemento Transport.                                                                                                         |
| [**\_acesso ao conjunto do alterador de IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Define o estado da porta de inserção/ejeção do dispositivo, porta ou teclado.                                                                                   |
| [**\_posição do conjunto de alterador de IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Define o mecanismo de transporte robótica do alterador para o endereço do elemento especificado.                                                                     |



 

Os códigos de controle a seguir são usados com o gerenciamento de dispositivos.



| Código de controle                                                                                      | Operação                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_verificação do armazenamento de IOCTLs \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Verifica a alteração em um dispositivo de mídia removível.                                                               |
| [**\_mídia de \_ ejeção do armazenamento do IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Ejeta a mídia de um dispositivo SCSI.                                                                             |
| [**\_controle de \_ ejeção de armazenamento de IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Habilita ou desabilita o mecanismo que ejeta a mídia.                                                         |
| [**armazenamento de IOCTL \_ \_ obter \_ número de dispositivo \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Recupera o tipo de dispositivo, o número do dispositivo e, para um dispositivo particionável, o número da partição de um dispositivo. |
| [**\_informações de \_ Get \_ HOTPLUG do armazenamento \_ do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Recupera a configuração de hotplug do dispositivo especificado.                                                 |
| [**armazenamento de IOCTL \_ \_ obter \_ número de série de mídia \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Recupera o número de série de um dispositivo USB.                                                                 |
| [**armazenamento de IOCTL \_ \_ obter \_ tipos de mídia \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Recupera as informações de geometria do dispositivo.                                                            |
| [**armazenamento de IOCTL \_ \_ obter tipos de mídia, por \_ \_ \_ exemplo**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Recupera informações sobre os tipos de mídia com suporte de um dispositivo.                                        |
| [**\_mídia de \_ carga de armazenamento de IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Carrega a mídia em um dispositivo.                                                                                   |
| [**\_atributos do \_ conjunto de dados de gerenciamento de armazenamento do \_ \_ IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_ \_ controle MCN de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Habilita ou desabilita a notificação de alteração de mídia.                                                               |
| [**\_remoção de \_ mídia de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Habilita ou desabilita o mecanismo de ejeção de mídia.                                                               |
| [**\_capacidade de \_ leitura do armazenamento do IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Recupera as informações de geometria para o dispositivo.                                                           |
| [**\_informações de \_ HOTPLUG do conjunto de armazenamento do IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Define a configuração de hotplug do dispositivo especificado.                                                      |



 

 

 



