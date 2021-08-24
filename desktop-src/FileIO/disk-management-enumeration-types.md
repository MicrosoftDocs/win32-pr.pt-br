---
description: Tipos de enumeração usados com o gerenciamento de disco.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Tipos de enumeração de gerenciamento de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765906"
---
# <a name="disk-management-enumeration-types"></a>Tipos de enumeração de gerenciamento de disco

Os tipos de enumeração a seguir são usados com o gerenciamento de disco.

## <a name="in-this-section"></a>Nesta seção



| Enumeração                                                                              | Descrição                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de mídia \_**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Representa as várias formas de mídia de dispositivo.<br/>                                                                                                                                                                                                                                                             |
| [**estilo de partição \_**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Representa o formato de uma partição.<br/>                                                                                                                                                                                                                                                                     |
| [**\_tipo de barramento de armazenamento \_**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Fornece um meio simbólico de representar tipos de barramento de armazenamento.<br/>                                                                                                                                                                                                                                              |
| [**\_status de \_ integridade do componente de armazenamento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Especifica o status de integridade de um componente de armazenamento.<br/>                                                                                                                                                                                                                                                       |
| [**\_ \_ fator forma de dispositivo de armazenamento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Especifica o fator forma de um dispositivo.<br/>                                                                                                                                                                                                                                                                    |
| [**\_unidades do \_ limite de energia do dispositivo de armazenamento \_ \_**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | As unidades do limite de energia máximo.<br/>                                                                                                                                                                                                                                                                 |
| [**\_conjunto de \_ códigos de porta de armazenamento \_**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Reservado para uso do sistema. <br/>                                                                                                                                                                                                                                                                                 |
| [**\_ID da propriedade de armazenamento \_**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Enumera os valores possíveis do membro **PropertyId** da estrutura de [**consulta de \_ propriedade \_ de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passada como entrada para a solicitação de [**\_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar as propriedades de um dispositivo ou adaptador de armazenamento.<br/> |
| [**\_tipo de protocolo de armazenamento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Especifica o protocolo de um dispositivo de armazenamento.<br/>                                                                                                                                                                                                                                                               |
| [**\_tipo de consulta de armazenamento \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Usado pela estrutura [**de \_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passada para o código de controle de [**\_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para indicar quais informações são retornadas sobre uma propriedade de um adaptador ou dispositivo de armazenamento.<br/>                             |
| [**\_alteração do cache de gravação \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indica se os recursos de cache de gravação de um dispositivo podem ser alterados.<br/>                                                                                                                                                                                                                                    |
| [**\_Habilitar cache de gravação \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indica se o cache de gravação está habilitado ou desabilitado.<br/>                                                                                                                                                                                                                                                 |
| [**\_tipo de cache de gravação \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Especifica o tipo de cache.<br/>                                                                                                                                                                                                                                                                                 |
| [**GRAVAÇÃO \_**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Especifica se um dispositivo de armazenamento dá suporte ao cache de write-through.<br/>                                                                                                                                                                                                                                        |



 

 

