---
title: Funções de prevenção contra perda de dados do ponto de extremidade
description: Funções usadas pelo recurso de prevenção contra perda de dados do ponto de extremidade.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f4a6395dacfdeccd032f7ad54719082c0e69f33692bda32798c09592c95d318e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751628"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Funções de prevenção contra perda de dados do ponto de extremidade

Funções usadas pelo recurso de prevenção contra perda de dados do ponto de extremidade.



| Funções                                                       | Descrição                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fornece ao sistema informações sobre um documento antes que a operação de fechamento do documento seja iniciada.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fornece ao sistema informações sobre um documento antes que a operação de fechamento do documento seja iniciada.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera a versão da API de DLP (Prevenção contra Perda de Dados) do ponto de extremidade no dispositivo atual.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica o sistema dos modos de imposição desejados para um conjunto de operações de DLP (Prevenção contra Perda de Dados) do ponto de extremidade.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina se o aplicativo deve receber os dados da área de transferência do sistema em vez de replicação de seu cache interno.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é exitado.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma cópia para a operação da área de transferência.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação aberta.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação aberta.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de colar da área de transferência.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fornece ao sistema informações sobre um documento após o início de uma operação de impressão.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fornece ao sistema informações de status após a conclusão de uma operação de área de transferência de stash.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento antes que uma operação de cópia para a área de transferência seja iniciada.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fornece ao sistema informações sobre um documento antes que uma operação de arrastar e soltar seja iniciada.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Fornece ao sistema informações sobre um documento antes que a operação aberta seja iniciada.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fornece ao sistema informações sobre um documento antes que a operação aberta seja iniciada.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fornece ao sistema informações sobre um documento antes que uma operação de colar da área de transferência seja iniciada.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fornece ao sistema informações sobre um documento antes que uma operação de impressão seja iniciada.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fornece ao sistema informações sobre um documento antes que uma operação salvar como seja iniciada.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.                                  |