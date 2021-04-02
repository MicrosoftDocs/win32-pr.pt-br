---
description: Quando o usuário inicia Visualizador de Eventos para exibir as entradas do log de eventos, ele chama a função ReadEventLog para obter as estruturas EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Exibindo o log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165446"
---
# <a name="viewing-the-event-log"></a>Exibindo o log de eventos

Quando o usuário inicia Visualizador de Eventos para exibir as entradas do log de eventos, ele chama a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para obter as estruturas [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . O Visualizador de Eventos usa a origem do evento e o identificador de evento para obter o texto da mensagem para cada evento do arquivo de mensagem registrado (indicado pelo valor do registro **EventMessageFile** para a origem). O Visualizador de Eventos usa a função [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para carregar o arquivo de mensagem. Em seguida, o Visualizador de Eventos usa a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para recuperar a cadeia de caracteres de descrição base do módulo carregado. Por fim, o Visualizador de Eventos substitui os parâmetros de inserção na cadeia de caracteres de descrição base para gerar a cadeia de caracteres final da mensagem.

 

 
