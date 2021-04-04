---
title: Funções de retorno de chamada ProjFS
description: As seguintes funções de retorno de chamada são declaradas em projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "103823531"
---
# <a name="callback-functions"></a>Funções de retorno de chamada

As seguintes funções de retorno de chamada são declaradas em projectedfslib. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Notifica o provedor de que uma operação por uma invocação anterior de um retorno de chamada deve ser cancelada. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informa ao provedor que uma enumeração de diretório está acima. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Solicita informações de enumeração de diretório do provedor.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Solicita o conteúdo do fluxo de dados primário de um arquivo.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Solicita informações para um arquivo ou diretório do provedor.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Fornece notificações para o provedor sobre operações do sistema de arquivos.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Determina se um determinado caminho de arquivo existe no repositório de backup do provedor.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informa ao provedor que uma enumeração de diretório está iniciando.