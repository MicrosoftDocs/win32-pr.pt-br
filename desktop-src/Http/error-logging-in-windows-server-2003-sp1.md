---
title: Log de erros no Windows Server 2003 SP1
description: Log de erros no Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Log de erros no Windows Server 2003 com Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2019
ms.locfileid: "103638848"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Log de erros no Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Adição de cabeçalhos de estilo W3C

A partir do Windows Server 2003 com Service Pack 1 (SP1), o log de erros da API do servidor HTTP inclui cabeçalhos de estilo W3C que permitem que os arquivos de log sejam analisados usando analisadores de log padrão. O modelo mostrado abaixo lista todos os campos que podem ser registrados no arquivo de log de erros http.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Registrando campos adicionais

O log de erros HTTP foi estendido para incluir mais nove campos para registrar dados sobre falhas que ocorrem. Os novos campos de erro são listados abaixo:

-   Nome do computador do servidor \[ S-computername\]
-   Agente \[ do usuário cs ( \_ agente do usuário)\]
-   \[Cs de cookie (cookie)\]
-   \[cs (referenciador) do referenciador\]
-   Nome do host \[ cs-host\]
-   Bytes recebidos pelo servidor \[ SC-bytes\]
-   Bytes recebidos e processados pelo servidor \[ cs-bytes\]
-   Tempo necessário para processar o tempo de solicitação \[ -Obtido\]
-   Queue-Name (reservado para IIS) \[ S-QueueName\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Selecionando arquivos para fazer logon no arquivo de log de erros HTTP

A chave do registro **ErrorLoggingFields** foi adicionada para controlar os campos registrados no log de erros http. Esses valores de registro estão localizados sob uma \\ chave de parâmetros http localizada em:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

O valor do registro **ErrorLoggingFields** é um valor DWORD que contém valores de bits para cada um dos campos que podem ser registrados. Para habilitar o registro em log de um campo específico, defina seu valor de bit correspondente como 1 e reinicie o serviço HTTP. Para desabilitar o registro em log, defina o valor de bit como 0. Para configurar vários campos, use um ou mais bits de valores individuais. Por exemplo, para ativar os campos de registro em log de cookies e referenciais, o valor deve ser 0x00020000 \| 0x00040000 = 0x00060000. Se a chave do registro **ErrorLoggingFields** estiver ausente, os campos padrão serão registrados. O valor de **ErrorLoggingFields** para registrar os campos padrão é 0x7c884c7. Para habilitar o registro em log para todos os campos mostrados na tabela abaixo, defina o valor como 0x7dff4e7.

Os campos de log de erros são listados na tabela a seguir:



| Campo de log            | Registrado por padrão | Valor de bit  |
|----------------------|-------------------|------------|
| Data                 | Sim               | 0x00000001 |
| Hora                 | Sim               | 0x00000002 |
| Nome do computador servidor | Não                | 0x00000020 |
| Endereço IP do Cliente    | Sim               | 0x00000004 |
| Porta do cliente          | Sim               | 0x00400000 |
| Endereço IP do servidor    | Sim               | 0x00000040 |
| Porta do servidor          | Sim               | 0x00008000 |
| Versão do protocolo     | Sim               | 0x00080000 |
| Método               | Sim               | 0x00000080 |
| URI                  | Sim               | 0x00800000 |
| Agente do usuário           | Não                | 0x00010000 |
| Cookie               | Não                | 0x00020000 |
| referenciador             | Não                | 0x00040000 |
| Host                 | Não                | 0x00100000 |
| Status do protocolo      | Sim               | 0x00000400 |
| SC-Bytes             | Não                | 0x00001000 |
| CS-Bytes             | Não                | 0x00002000 |
| Tempo decorrido           | Não                | 0x00004000 |
| SiteId               | Sim               | 0x01000000 |
| Frase do motivo        | Sim               | 0x02000000 |
| Nome da fila           | Não                | 0x04000000 |
| ID do fluxo            | Não                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Substituição de data e hora

Por padrão, um novo arquivo de log de erros HTTP é criado (substituição de arquivo com prazo) quando o arquivo de log atual atinge um tamanho especificado. A partir do Windows Server 2003 com SP1, novos arquivos de log de erros podem ser criados com base na data e hora. A substituição de hora e de data é controlada por dois novos valores de registro: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover**. Para habilitar a substituição de data e hora, esses valores de registro devem ser adicionados ao registro. O serviço http deve ser reiniciado quando essas chaves são adicionadas ao registro. As chaves do registro de substituição do arquivo de log são criadas sob a seguinte chave:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

A chave do registro **ErrorLoggingRolloverType** indica o tipo de substituição desejado e é definida por padrão como a substituição baseada em tamanho. A substituição também pode ser definida para ocorrer em uma base diária, semanal, mensal ou por hora. Quando a substituição de arquivo é baseada no tempo, um valor de **ErrorLoggingLocaltimeRollover** de 0 indica que o tempo de substituição é expresso em GMT e um valor de 1 indica que o tempo de substituição é expresso na hora local. A chave **ErrorLoggingRolloverType** pode usar um valor de 0 a 4, conforme listado na tabela a seguir.



| Valor do tipo de substituição | Descrição                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Substituição baseada em tamanho. Os arquivos de log são substituídos quando o arquivo atinge o tamanho definido na chave do registro **ErrorLogFileTruncateSize** . |
| 1                   | A substituição do arquivo de log ocorre diariamente.                                                                                                         |
| 2                   | A substituição do arquivo de log ocorre semanalmente.                                                                                                        |
| 3                   | A substituição do arquivo de log ocorre mensalmente.                                                                                                       |
| 4                   | A substituição do arquivo de log ocorre por hora.                                                                                                        |



 

As convenções de nomenclatura para arquivos que armazenam os logs de erros são diferentes para o tamanho, a data e a substituição baseada em tempo. A tabela a seguir lista as convenções de nomenclatura para arquivos de log http.



| Tipo de Tollover | Nome do arquivo de log  | Descrição                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Tamanho          | HTTPERRn. LOG   | O arquivo de log é reciclado quando atinge um tamanho específico. n é o número do arquivo e é incrementado quando o arquivo de log é substituído. |
| Diariamente         | htYYMMDD. log   | O arquivo de log é reciclado diariamente.                                                                                                     |
| Semanalmente        | htYYMMww. log   | O arquivo de log é reciclado semanalmente, em que WW é a semana do mês.                                                                 |
| Mensal       | htYYMM. log     | O arquivo de log é reciclado a cada mês.                                                                                               |
| A cada hora        | htYYMMDDhh. log | O arquivo de log é reciclado por hora, em que HH é a hora do dia expressa em notação de 0-24 horas.                                   |



 

 

 




