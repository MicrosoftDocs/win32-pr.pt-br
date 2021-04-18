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
# <a name="logging-and-error-reporting"></a><span data-ttu-id="cf72b-103">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="cf72b-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="cf72b-104">Arquivo de log</span><span class="sxs-lookup"><span data-stu-id="cf72b-104">Log file</span></span>

<span data-ttu-id="cf72b-105">COMREPL gera um arquivo de log contendo mensagens de status e de erro.</span><span class="sxs-lookup"><span data-stu-id="cf72b-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="cf72b-106">Esse arquivo é armazenado no computador em que COMREPL foi iniciado em% systemdir% \\ com \\ Replication \\ COMREPL. log.</span><span class="sxs-lookup"><span data-stu-id="cf72b-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="cf72b-107">Esse arquivo de log é limpo quando uma fase de cópia é iniciada.</span><span class="sxs-lookup"><span data-stu-id="cf72b-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="cf72b-108">A instalação subsequente nos destinos será acrescentada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf72b-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="cf72b-109">Tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="cf72b-109">Error handling</span></span>

<span data-ttu-id="cf72b-110">Os erros são observados no arquivo de log descrito acima.</span><span class="sxs-lookup"><span data-stu-id="cf72b-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="cf72b-111">Informações detalhadas sobre o erro também podem ser encontradas no log de eventos nos computadores de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="cf72b-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf72b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf72b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf72b-113">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="cf72b-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="cf72b-114">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="cf72b-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="cf72b-115">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="cf72b-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="cf72b-116">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="cf72b-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



