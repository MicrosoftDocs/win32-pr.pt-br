---
description: Cada log de eventos contém um título (representado pela estrutura ELF LOGFILE HEADER) que tem um tamanho fixo, seguido por um número variável de registros de evento (representados por estruturas \_ EVENTLOGRECORD) e um registro de fim de arquivo (representado pela estrutura \_ \_ ELF EOF \_ RECORD).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato de arquivo de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ed6df35ac1fcd641a9a895b2c32eb34d6a4c1cb472ab03f16417f55900c767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814284"
---
# <a name="event-log-file-format"></a>Formato de arquivo de log de eventos

Cada log de eventos contém um título (representado pela estrutura [**ELF \_ LOGFILE \_ HEADER)**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) que tem um tamanho fixo, seguido por um número variável de registros de evento (representados por estruturas [**EVENTLOGRECORD)**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) e um registro de fim de arquivo (representado pela estrutura [**ELF \_ EOF \_ RECORD).**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85))

A **estrutura ELF \_ LOGFILE \_ HEADER** e a estrutura **ELF \_ EOF \_ RECORD** são escritas no log de eventos quando o log de eventos é criado e atualizado sempre que um evento é gravado no log.

Quando um aplicativo chama a [**função ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) para gravar uma entrada no log de eventos, o sistema passa os parâmetros para o serviço de registro em log de eventos. O serviço de registro em log de eventos usa as informações para gravar uma **estrutura EVENTLOGRECORD** no log de eventos. O diagrama a seguir ilustra esse processo.

![escrevendo um arquivo de log](images/evreport.png)

Os registros de evento são organizados de uma das seguintes maneiras:

-   Não envolvendo. O registro mais antigo é imediatamente após o header do log de eventos e novos registros são adicionados após o último registro que foi adicionado (antes do **ELF \_ EOF \_ RECORD**). O exemplo a seguir mostra o método que não envolve:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    O não quebra-quebra pode ocorrer quando o log de eventos é criado ou quando o log de eventos é limpo. O log de eventos continua não sendo empacotado até que o limite de tamanho do log de eventos seja atingido. O tamanho do log de eventos é limitado pelo valor de **configuração MaxSize** ou pela quantidade de recursos do sistema.

    Quando o limite de tamanho do log de eventos é atingido, ele pode começar a ser empacotado. O empacotamento é controlado pelo **valor de configuração** retenção. Para obter mais informações sobre os valores de configuração do log de eventos, consulte [Eventlog Key](eventlog-key.md).

-   Envolvimento. Os registros são organizados como um buffer circular. À medida que novos registros são adicionados, os registros mais antigos são substituídos. O local dos registros mais antigos e mais novos variará. O exemplo a seguir mostra o método de empacotamento.

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

    No exemplo, o registro mais antigo não é mais 1, mas é 102 porque o espaço para registros de 1 a 101 foi substituído.

    Há algum espaço entre o **REGISTRO \_ ELF EOF \_** e o registro mais antigo porque o sistema apagará um número integral de registros para liberar espaço para o registro mais recente. Por exemplo, se o registro mais recente tiver 100 bytes e os dois registros mais antigos tiverem 75 bytes, o sistema removerá os dois registros mais antigos. Os 50 bytes extras serão usados posteriormente quando novos registros são gravados.

    Um arquivo de log de eventos tem um tamanho fixo e, quando os registros no wrap de arquivo, o registro no final do arquivo normalmente será dividido em dois registros. Por exemplo, se a posição para a próxima gravação for de 100 bytes do final do arquivo e o tamanho do registro for 300 bytes, os primeiros 100 bytes serão gravados no final do arquivo e os próximos 200 bytes serão gravados no início do arquivo imediatamente após o TÍTULO **\_ ELF LOGFILE \_**. Se o espaço disponível no final do arquivo for menor que a parte fixa do **EVENTLOGRECORD** (0x38 bytes), todo o novo registro será gravado no início do arquivo imediatamente após o **\_ \_ HEADER ELF LOGFILE**. Os bytes não usadas no final do arquivo serão preenchidos com o padrão 0x00000027.

Para obter mais informações e um exemplo de código, consulte [Relatando um evento](reporting-an-event.md).

 

 
