---
description: As funções a seguir são usadas com o log de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funções de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787119"
---
# <a name="event-logging-functions"></a><span data-ttu-id="bb394-103">Funções de log de eventos</span><span class="sxs-lookup"><span data-stu-id="bb394-103">Event Logging Functions</span></span>

<span data-ttu-id="bb394-104">As funções a seguir são usadas com o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bb394-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="bb394-105">Função</span><span class="sxs-lookup"><span data-stu-id="bb394-105">Function</span></span>                                                         | <span data-ttu-id="bb394-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb394-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb394-107">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="bb394-108">Salva o log de eventos especificado em um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="bb394-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="bb394-109">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="bb394-110">Limpa o log de eventos especificado e, opcionalmente, salva a cópia atual do log em um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="bb394-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="bb394-111">**CloseEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="bb394-112">Fecha um identificador de leitura para o log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="bb394-113">**DeregisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="bb394-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="bb394-114">Fecha um identificador de gravação no log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="bb394-115">**GetEventLogInformation**</span><span class="sxs-lookup"><span data-stu-id="bb394-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="bb394-116">Recupera informações sobre o log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="bb394-117">**GetNumberOfEventLogRecords**</span><span class="sxs-lookup"><span data-stu-id="bb394-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="bb394-118">Recupera o número de registros no log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="bb394-119">**GetOldestEventLogRecord**</span><span class="sxs-lookup"><span data-stu-id="bb394-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="bb394-120">Recupera o número de registro absoluto do registro mais antigo no log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="bb394-121">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="bb394-122">Permite que um aplicativo receba notificação quando um evento é gravado no log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="bb394-123">**OpenBackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="bb394-124">Abre um identificador para um log de eventos de backup.</span><span class="sxs-lookup"><span data-stu-id="bb394-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="bb394-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="bb394-126">Abre um identificador para o log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="bb394-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="bb394-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="bb394-128">Lê um número inteiro de entradas do log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="bb394-129">**RegisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="bb394-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="bb394-130">Recupera um identificador registrado para o log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="bb394-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="bb394-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="bb394-132">Grava uma entrada no final do log de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="bb394-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



