---
title: Funções de prevenção de perda de dados do ponto de extremidade
description: Funções usadas pelo recurso de prevenção de perda de dados do ponto de extremidade.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f8713a6a6051bf477b4f9c7f6f8a7430abf70a52
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495311"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Funções de prevenção de perda de dados do ponto de extremidade

Funções usadas pelo recurso de prevenção de perda de dados do ponto de extremidade.



| Funções                                                       | Descrição                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é encerrado.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação colar da área de transferência.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fornece ao sistema informações sobre um documento após o início de uma operação de impressão.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação de cópia para a área de transferência ser iniciada.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação arrastar e soltar ser iniciada.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação colar da área de transferência ser iniciada.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fornece ao sistema informações sobre um documento antes de uma operação salvar como ser iniciada.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.                                  |