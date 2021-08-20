---
title: Log de erros no Windows Server 2003 SP1
description: Log de erros no Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Log de erros no Windows Server 2003 com Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014804"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Log de erros no Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Adição de títulos de estilo W3C

A partir do Windows Server 2003 com Service Pack 1 (SP1), o log de erros da API do Servidor HTTP inclui cabeçalhos de estilo W3C, permitindo que os arquivos de log sejam analisados usando analisadores de log padrão. O modelo mostrado abaixo lista todos os campos que podem ser registrados no arquivo de log de erros http.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Registrando em log campos adicionais

O log de erros HTTP foi estendido para incluir mais nove campos para registrar dados sobre falhas que ocorrem. Os novos campos de erro são listados abaixo:

-   Nome do computador do \[ servidor S-COMPUTERNAME\]
-   User Agent \[ CS(USER \_ AGENT)\]
-   Cookie \[ CS(COOKIE)\]
-   referrer \[ CS(referrer)\]
-   Nome do host \[ CS-HOST\]
-   Bytes recebidos pelo \[ SERVIDOR SC-BYTES\]
-   Bytes recebidos e processados pelo \[ servidor CS-BYTES\]
-   Tempo levado para processar a \[ solicitação TIME-TAKEN\]
-   Queue-Name (Reservado para IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selecionando arquivos arquivados para fazer logoff no arquivo de log de erros HTTP

A **chave do Registro ErrorLoggingFields** foi adicionada para controlar os campos registrados no log de erros HTTP. Esses valores do Registro estão localizados em uma chave de Parâmetros HTTP \\ localizada em:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

O **valor do registro ErrorLoggingFields** é um valor DWORD que contém valores de bit para cada um dos campos que podem ser registrados. Para habilitar o registro em log de um campo específico, de definido seu valor de bit correspondente como 1 e reinicie o serviço HTTP. Para desabilitar o registro em log, de definido o valor de bit como 0. Para configurar vários campos, use um OR bit a bit dos valores individuais. Por exemplo, para ativar os campos de log Cookie e Referrer, o valor deve ser 0x00020000 \| 0x00040000 = 0x00060000. Se a **chave do Registro ErrorLoggingFields** estiver ausente, os campos padrão serão registrados. O **valor ErrorLoggingFields** para registrar os campos padrão é 0x7c884c7. Para habilitar o registro em log para todos os campos mostrados na tabela abaixo, de definir o valor como 0x7dff4e7.

Os campos de log de erros são listados na tabela a seguir:



| Campo de log            | Registrado por padrão | Valor de bit  |
|----------------------|-------------------|------------|
| Data                 | Sim               | 0x00000001 |
| Tempo                 | Sim               | 0x00000002 |
| Nome do computador do servidor | Não                | 0x00000020 |
| Endereço IP do Cliente    | Sim               | 0x00000004 |
| Porta do cliente          | Sim               | 0x00400000 |
| Endereço IP do servidor    | Sim               | 0x00000040 |
| Porta do servidor          | Sim               | 0x00008000 |
| Versão do protocolo     | Sim               | 0x00080000 |
| Método               | Sim               | 0x00000080 |
| URI                  | Sim               | 0x00800000 |
| Agente do usuário           | Não                | 0x00010000 |
| Cookie               | Não                | 0x00020000 |
| Referrer             | Não                | 0x00040000 |
| Host                 | Não                | 0x00100000 |
| Status do protocolo      | Sim               | 0x00000400 |
| SC-Bytes             | Não                | 0x00001000 |
| CS-Bytes             | Não                | 0x00002000 |
| Tempo decorrido           | Não                | 0x00004000 |
| Siteid               | Sim               | 0x01000000 |
| Frase de motivo        | Sim               | 0x02000000 |
| Nome da fila           | Não                | 0x04000000 |
| ID do fluxo            | Não                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Rollover de data e hora

Por padrão, um novo arquivo de log de erros HTTP é criado (chamada de sobreover de arquivo) quando o arquivo de log atual atinge um tamanho especificado. A partir do Windows Server 2003 com SP1, novos arquivos de log de erros podem ser criados com base na data e hora. A recalculação de data e hora é controlada por dois novos valores do Registro: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover**. Para habilitar a sobreção de data e hora, esses valores do Registro devem ser adicionados ao Registro. O serviço Http deve ser reiniciado quando essas chaves são adicionadas ao Registro. As chaves do Registro de sobrepondo arquivo de log são criadas sob a seguinte chave:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

A **chave do Registro ErrorLoggingRolloverType** indica o tipo de sobrepondo desejado e é definida por padrão como sobressalente baseada em tamanho. A sobrepondo também pode ser definida para ocorrer diariamente, semanalmente, mensalmente ou por hora. Quando a sobrepondo de arquivo é baseada no tempo, um valor **errorLoggingLocaltimeRollover** de 0 indica que o tempo de sobressalto é expresso em GMT e um valor de 1 indica que o tempo de sobressalto é expresso em hora local. A **chave ErrorLoggingRolloverType** pode ter um valor de 0 a 4, conforme listado na tabela a seguir.



| Valor do tipo de sobressempo | Descrição                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Sobrepondo com base no tamanho. Os arquivos de log são rolados quando o arquivo atinge o tamanho definido na chave do Registro **ErrorLogFileTruncateSize.** |
| 1                   | A sobreção de arquivo de log ocorre diariamente.                                                                                                         |
| 2                   | A sobreção do arquivo de log ocorre semanalmente.                                                                                                        |
| 3                   | A sobreção de arquivo de log ocorre mensalmente.                                                                                                       |
| 4                   | A sobrepondo de arquivo de log ocorre por hora.                                                                                                        |



 

As convenções de nomen por arquivos que armazenam os logs de erro são diferentes para a sobrepondo com base no tamanho, na data e na hora. A tabela a seguir lista as convenções de nomen por arquivos de log Http.



| Tipo de pedágio | Nome do arquivo de log  | Descrição                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Tamanho          | HTTPERRn.LOG   | O arquivo de log é reciclado quando atinge um tamanho específico. n é o número do arquivo e é incrementado quando o arquivo de log é sobrecarrado. |
| Diariamente         | htYYMMDD.log   | O arquivo de log é reciclado diariamente.                                                                                                     |
| Semanalmente        | htYYMMww.log   | O arquivo de log é reciclado semanalmente, em que ww é a semana do mês.                                                                 |
| Mensal       | htYYMM.log     | O arquivo de log é reciclado todos os meses.                                                                                               |
| A cada hora        | htYYMMDDhh.log | O arquivo de log é reciclado por hora, em que hh é a hora do dia expressa em notação de 0 a 24 horas.                                   |



 

 

 




