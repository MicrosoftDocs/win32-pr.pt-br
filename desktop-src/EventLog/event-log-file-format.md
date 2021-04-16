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
# <a name="event-log-file-format"></a>Formato do arquivo de log de eventos

Cada log de eventos contém um cabeçalho (representado pela estrutura de [**\_ \_ cabeçalho**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) do arquivo ELF) que tem um tamanho fixo, seguido por um número variável de registros de eventos (representado por estruturas [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) e um registro de fim de arquivo (representado pela estrutura de [**\_ \_ registro Elf EOF**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).

A estrutura de cabeçalho do arquivo de **\_ log \_ Elf** e a estrutura de **\_ \_ registro Elf EOF** são gravadas no log de eventos quando o log de eventos é criado e são atualizados sempre que um evento é gravado no log.

Quando um aplicativo chama a função [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para gravar uma entrada no log de eventos, o sistema passa os parâmetros para o serviço de log de eventos. O serviço de log de eventos usa as informações para gravar uma estrutura **EVENTLOGRECORD** no log de eventos. O diagrama a seguir ilustra esse processo.

![gravando um arquivo de log](images/evreport.png)

Os registros de eventos são organizados de uma das seguintes maneiras:

-   Sem quebra automática. O registro mais antigo é imediatamente após o cabeçalho do log de eventos e novos registros são adicionados após o último registro que foi adicionado (antes do **\_ \_ registro de EOF Elf**). O exemplo a seguir mostra o método sem quebra automática:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    A não disposição pode ocorrer quando o log de eventos é criado ou quando o log de eventos é limpo. O log de eventos continua a ser sem encapsulamento até que o limite de tamanho do log de eventos seja atingido. O tamanho do log de eventos é limitado pelo valor de configuração **MaxSize** ou pela quantidade de recursos do sistema.

    Quando o limite de tamanho do log de eventos é atingido, ele pode iniciar o encapsulamento. O encapsulamento é controlado pelo valor de configuração de **retenção** . Para obter mais informações sobre os valores de configuração do log de eventos, consulte a [chave EventLog](eventlog-key.md).

-   Encapsulamento. Os registros são organizados como um buffer circular. À medida que novos registros são adicionados, os registros mais antigos são substituídos. O local dos registros mais antigos e mais recentes varia. O exemplo a seguir mostra o método de disposição.

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

    No exemplo, o registro mais antigo não é mais 1, mas é 102 porque o espaço para os registros de 1 a 101 foi substituído.

    Há algum espaço entre o **registro Elf \_ EOF \_** e o registro mais antigo, pois o sistema apagará um número integral de registros para liberar espaço para o registro mais recente. Por exemplo, se o registro mais recente tiver 100 bytes de comprimento e os dois registros mais antigos tiverem 75 bytes de comprimento, o sistema removerá os dois registros mais antigos. Os 50 bytes adicionais serão usados posteriormente quando novos registros forem gravados.

    Um arquivo de log de eventos tem um tamanho fixo e, quando os registros no arquivo são encapsulados, o registro no final do arquivo normalmente é dividido em dois registros. Por exemplo, se a posição da próxima gravação for de 100 bytes a partir do final do arquivo e o tamanho do registro for de 300 bytes, os primeiros 100 bytes serão gravados no final do arquivo e os próximos 200 bytes serão gravados no início do arquivo imediatamente após o **\_ \_ cabeçalho de log** de arquivos ELF. Se o espaço disponível no final do arquivo for menor que a parte fixa do **EVENTLOGRECORD** (0x38 bytes), todo o novo registro será gravado no início do arquivo imediatamente após o **cabeçalho de \_ log \_** de arquivos ELF. Os bytes não utilizados no final do arquivo serão preenchidos com o padrão 0x00000027.

Para obter mais informações e um exemplo de código, consulte [relatando um evento](reporting-an-event.md).

 

 
