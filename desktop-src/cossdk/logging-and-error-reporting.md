---
description: Registro em log e relatório de erros
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registro em log e relatório de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990756"
---
# <a name="logging-and-error-reporting"></a>Registro em log e relatório de erros

## <a name="log-file"></a>Arquivo de log

COMREPL gera um arquivo de log que contém mensagens de status e de erro. Esse arquivo é armazenado no computador em que COMREPL foi lançado em %systemdir% \\ com \\ replication \\ ComRepl.log.

Esse arquivo de log é limpo quando uma fase de cópia é iniciada. A instalação subsequente nos destinos será anexada ao arquivo.

## <a name="error-handling"></a>Tratamento de erros

Os erros são notados no arquivo de log descrito acima. Informações de erro detalhadas também podem ser encontradas no log de eventos em computadores de origem ou de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Arquivos](file-management.md)
</dt> <dt>

[Fases de replicação](replication-phases.md)
</dt> <dt>

[Usando COMREPL](using-comrepl.md)
</dt> <dt>

[O que é replicado](what-gets-replicated.md)
</dt> </dl>

 

 



