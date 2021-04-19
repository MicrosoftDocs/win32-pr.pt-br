---
description: Cada log na chave EventLog contém subchaves chamadas fontes de eventos. A origem do evento é o nome do software que registra o evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Origens de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780548"
---
# <a name="event-sources"></a>Origens de eventos

Cada log na [chave EventLog](eventlog-key.md) contém subchaves chamadas *fontes de eventos*. A origem do evento é o nome do software que registra o evento. Geralmente, é o nome do aplicativo ou o nome de um subcomponente do aplicativo se o aplicativo for grande. Você pode adicionar um máximo de 16.384 origens de eventos ao registro. O log de **segurança** é somente para uso do sistema. Os drivers de dispositivo devem adicionar seus nomes ao log do **sistema** . Os aplicativos e serviços devem adicionar seus nomes ao log do **aplicativo** ou criar um log personalizado.

A estrutura das origens do evento é a seguinte:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

Você não pode usar um nome de origem que já tenha sido usado como um nome de log. Além disso, os nomes de origem não podem ser hierárquicos; ou seja, eles não podem conter o caractere de barra invertida (" \\ ").

Cada origem de evento contém informações (como um [arquivo de mensagem](message-files.md)) específicas para o software que registrará os eventos, conforme mostrado na tabela a seguir.



<table>
<thead>
<tr class="header">
<th>Valor do registro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>Número de categorias de eventos com suporte. Esse valor é do tipo <strong>REG_DWORD</strong>.</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>Caminho para o arquivo de mensagem de categoria. Um arquivo de mensagem de categoria contém cadeias de caracteres dependentes de idioma que descrevem as categorias. Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>Caminho para um ou mais arquivos de mensagem de evento; Use um ponto e vírgula para delimitar vários arquivos. Um arquivo de mensagem de evento contém cadeias de caracteres dependentes de idioma que descrevem os eventos. Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>Caminho para o arquivo de mensagem de parâmetro. Um arquivo de mensagem de parâmetro contém cadeias de caracteres independentes de idioma que devem ser inseridas nas cadeias de caracteres de descrição do evento. Esse valor pode ser do tipo <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>Bitmask de tipos com suporte. Esse valor é do tipo <strong>REG_DWORD</strong>. Pode ser um ou mais dos seguintes valores: <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)<br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)<br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)<br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)<br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)<br />
</dl></td>
</tr>
</tbody>
</table>



 

Quando um aplicativo usa a função [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para obter um identificador para um log de eventos, o serviço de log de eventos pesquisa a origem do evento especificado no registro. Por exemplo, o log do **aplicativo** pode conter fontes de eventos para Microsoft SQL Server e o Microsoft Excel. Se um aplicativo usar [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou **OpenEventLog** com um nome de origem de aplicativo, SQL ou Excel, o serviço de log de eventos retornará um identificador para o log do **aplicativo** .

Um aplicativo pode usar o log do **aplicativo** sem adicionar uma nova origem do evento ao registro. Se o aplicativo chamar [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) e passar um nome de origem que não pode ser encontrado no registro, o serviço de log de eventos usará o log do **aplicativo** por padrão. No entanto, como não há nenhum arquivo de mensagem, o Visualizador de Eventos não pode mapear nenhum identificador de evento ou categorias de evento para uma cadeia de caracteres de descrição e exibirá um erro. Por esse motivo, você deve adicionar uma origem de evento exclusiva ao registro para seu aplicativo e especificar um arquivo de mensagem.

 

 



