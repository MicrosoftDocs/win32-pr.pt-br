---
title: Funções de retorno de chamada do ProjFS
description: As seguintes funções de retorno de chamada são declaradas em projectedfslib.h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 595fac418ce57e1e6caff718d75b458390efd31c2e8727cd2feb8ee5a5d86eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031156"
---
# <a name="callback-functions"></a>Funções de retorno de chamada

As seguintes funções de retorno de chamada são declaradas em projectedfslib.h.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Notifica o provedor de que uma operação por uma invocação anterior de um retorno de chamada deve ser cancelada. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informa ao provedor que uma enumeração de diretório terminou. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Solicita informações de enumeração de diretório do provedor.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Solicita o conteúdo do fluxo de dados primário de um arquivo.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Solicita informações para um arquivo ou diretório do provedor.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Fornece notificações ao provedor sobre operações do sistema de arquivos.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Determina se um determinado caminho de arquivo existe no armazenamento de backing do provedor.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informa ao provedor que uma enumeração de diretório está iniciando.