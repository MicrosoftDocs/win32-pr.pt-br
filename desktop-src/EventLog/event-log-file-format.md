---
description: Cada log de eventos contém um cabeçalho (representado pela estrutura de cabeçalho do arquivo ELF \_ \_ ) que tem um tamanho fixo, seguido por um número variável de registros de eventos (representado por estruturas EVENTLOGRECORD) e um registro de fim de arquivo (representado pela \_ estrutura de registro Elf EOF \_ ).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato do arquivo de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505760"
---
# <a name="event-log-file-format"></a><span data-ttu-id="a029b-103">Formato do arquivo de log de eventos</span><span class="sxs-lookup"><span data-stu-id="a029b-103">Event Log File Format</span></span>

<span data-ttu-id="a029b-104">Cada log de eventos contém um cabeçalho (representado pela estrutura de [**\_ \_ cabeçalho**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) do arquivo ELF) que tem um tamanho fixo, seguido por um número variável de registros de eventos (representado por estruturas [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) e um registro de fim de arquivo (representado pela estrutura de [**\_ \_ registro Elf EOF**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).</span><span class="sxs-lookup"><span data-stu-id="a029b-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="a029b-105">A estrutura de cabeçalho do arquivo de **\_ log \_ Elf** e a estrutura de **\_ \_ registro Elf EOF** são gravadas no log de eventos quando o log de eventos é criado e são atualizados sempre que um evento é gravado no log.</span><span class="sxs-lookup"><span data-stu-id="a029b-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="a029b-106">Quando um aplicativo chama a função [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para gravar uma entrada no log de eventos, o sistema passa os parâmetros para o serviço de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="a029b-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="a029b-107">O serviço de log de eventos usa as informações para gravar uma estrutura **EVENTLOGRECORD** no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="a029b-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="a029b-108">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="a029b-108">The following diagram illustrates this process.</span></span>

![gravando um arquivo de log](images/evreport.png)

<span data-ttu-id="a029b-110">Os registros de eventos são organizados de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="a029b-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="a029b-111">Sem quebra automática.</span><span class="sxs-lookup"><span data-stu-id="a029b-111">Non-wrapping.</span></span> <span data-ttu-id="a029b-112">O registro mais antigo é imediatamente após o cabeçalho do log de eventos e novos registros são adicionados após o último registro que foi adicionado (antes do **\_ \_ registro de EOF Elf**).</span><span class="sxs-lookup"><span data-stu-id="a029b-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="a029b-113">O exemplo a seguir mostra o método sem quebra automática:</span><span class="sxs-lookup"><span data-stu-id="a029b-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="a029b-114">A não disposição pode ocorrer quando o log de eventos é criado ou quando o log de eventos é limpo.</span><span class="sxs-lookup"><span data-stu-id="a029b-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="a029b-115">O log de eventos continua a ser sem encapsulamento até que o limite de tamanho do log de eventos seja atingido.</span><span class="sxs-lookup"><span data-stu-id="a029b-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="a029b-116">O tamanho do log de eventos é limitado pelo valor de configuração **MaxSize** ou pela quantidade de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="a029b-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="a029b-117">Quando o limite de tamanho do log de eventos é atingido, ele pode iniciar o encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="a029b-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="a029b-118">O encapsulamento é controlado pelo valor de configuração de **retenção** .</span><span class="sxs-lookup"><span data-stu-id="a029b-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="a029b-119">Para obter mais informações sobre os valores de configuração do log de eventos, consulte a [chave EventLog](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="a029b-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="a029b-120">Encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="a029b-120">Wrapping.</span></span> <span data-ttu-id="a029b-121">Os registros são organizados como um buffer circular.</span><span class="sxs-lookup"><span data-stu-id="a029b-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="a029b-122">À medida que novos registros são adicionados, os registros mais antigos são substituídos.</span><span class="sxs-lookup"><span data-stu-id="a029b-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="a029b-123">O local dos registros mais antigos e mais recentes varia.</span><span class="sxs-lookup"><span data-stu-id="a029b-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="a029b-124">O exemplo a seguir mostra o método de disposição.</span><span class="sxs-lookup"><span data-stu-id="a029b-124">The following example shows the wrapping method.</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    <span data-ttu-id="a029b-125">No exemplo, o registro mais antigo não é mais 1, mas é 102 porque o espaço para os registros de 1 a 101 foi substituído.</span><span class="sxs-lookup"><span data-stu-id="a029b-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="a029b-126">Há algum espaço entre o **registro Elf \_ EOF \_** e o registro mais antigo, pois o sistema apagará um número integral de registros para liberar espaço para o registro mais recente.</span><span class="sxs-lookup"><span data-stu-id="a029b-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="a029b-127">Por exemplo, se o registro mais recente tiver 100 bytes de comprimento e os dois registros mais antigos tiverem 75 bytes de comprimento, o sistema removerá os dois registros mais antigos.</span><span class="sxs-lookup"><span data-stu-id="a029b-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="a029b-128">Os 50 bytes adicionais serão usados posteriormente quando novos registros forem gravados.</span><span class="sxs-lookup"><span data-stu-id="a029b-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="a029b-129">Um arquivo de log de eventos tem um tamanho fixo e, quando os registros no arquivo são encapsulados, o registro no final do arquivo normalmente é dividido em dois registros.</span><span class="sxs-lookup"><span data-stu-id="a029b-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="a029b-130">Por exemplo, se a posição da próxima gravação for de 100 bytes a partir do final do arquivo e o tamanho do registro for de 300 bytes, os primeiros 100 bytes serão gravados no final do arquivo e os próximos 200 bytes serão gravados no início do arquivo imediatamente após o **\_ \_ cabeçalho de log** de arquivos ELF.</span><span class="sxs-lookup"><span data-stu-id="a029b-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="a029b-131">Se o espaço disponível no final do arquivo for menor que a parte fixa do **EVENTLOGRECORD** (0x38 bytes), todo o novo registro será gravado no início do arquivo imediatamente após o **cabeçalho de \_ log \_** de arquivos ELF.</span><span class="sxs-lookup"><span data-stu-id="a029b-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="a029b-132">Os bytes não utilizados no final do arquivo serão preenchidos com o padrão 0x00000027.</span><span class="sxs-lookup"><span data-stu-id="a029b-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="a029b-133">Para obter mais informações e um exemplo de código, consulte [relatando um evento](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a029b-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
