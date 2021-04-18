---
description: Registro em log e relatório de erros
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registro em log e relatório de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781013"
---
# <a name="logging-and-error-reporting"></a>Registro em log e relatório de erros

## <a name="log-file"></a>Arquivo de log

COMREPL gera um arquivo de log contendo mensagens de status e de erro. Esse arquivo é armazenado no computador em que COMREPL foi iniciado em% systemdir% \\ com \\ Replication \\ COMREPL. log.

Esse arquivo de log é limpo quando uma fase de cópia é iniciada. A instalação subsequente nos destinos será acrescentada ao arquivo.

## <a name="error-handling"></a>Tratamento de erros

Os erros são observados no arquivo de log descrito acima. Informações detalhadas sobre o erro também podem ser encontradas no log de eventos nos computadores de origem ou de destino.

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

 

 



