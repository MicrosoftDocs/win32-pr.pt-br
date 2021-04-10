---
description: A API de script para referência de WMI descreve cada objeto de script usando uma sintaxe específica. Para obter uma explicação dessa sintaxe, consulte Convenções de documento para a API de script.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Objetos de API de script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165207"
---
# <a name="scripting-api-objects"></a>Objetos de API de script

A API de script para referência de WMI descreve cada objeto de script usando uma sintaxe específica. Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

A tabela a seguir lista os objetos de script WMI e como eles são usados.



| Objeto                                               | Descrição                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Constrói e analisa valores de [data e hora](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Recupera eventos em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Fornece informações de erro estendidas quando ocorre um erro.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Obtém um objeto [**SWbemServices**](swbemservices.md) que pode obter acesso ao WMI em um computador host específico.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contém uma única definição de método WMI.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Obtém uma coleção de objetos [**SWbemMethod**](swbemmethod.md) .                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contém um único valor nomeado.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Obtém acesso a uma coleção de objetos [**SWbemNamedValue**](swbemnamedvalue.md) .                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | Contém e manipula uma única classe ou instância de objeto WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Estende a funcionalidade de [**SWbemObject**](swbemobject.md). Esse objeto adiciona o método [**Refresh**](swbemrefresher-refresh.md) para objetos [**SWbemRefresher**](swbemrefresher.md) .                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Gera e valida um caminho de objeto.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Obtém acesso a uma coleção de objetos [**SWbemObject**](swbemobject.md) .                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Define ou limpa um privilégio.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Obtém acesso a uma coleção de objetos [**SWbemPrivilege**](swbemprivilege.md) .                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Contém uma única propriedade WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Obtém acesso a uma coleção de objetos [**SWbemProperty**](swbemproperty.md) .                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Contém um único qualificador de propriedade.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Obtém acesso a uma coleção de objetos [**SWbemQualifier**](swbemqualifier.md) .                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Coleta e atualiza valores de propriedade de objeto em uma única operação.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Representa um único elemento atualizável em um objeto [**SWbemRefresher**](swbemrefresher.md) , como uma propriedade.                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Gerencia configurações de segurança, como [**privilégios**](swbemsecurity-privileges.md)de Component Object Model (com), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)e [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md).   |
| [**SWbemServices**](swbemservices.md)               | Cria, atualiza e recupera instâncias ou classes.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Estende a funcionalidade do [**SWbemServices**](swbemservices.md). Esse objeto adiciona os métodos [**Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) para permitir que uma classe ou instância seja salva em vários namespaces. |
| [**SWbemSink**](swbemsink.md)                       | Recebe os resultados de operações assíncronas e notificações de eventos, que são usadas por aplicativos cliente.                                                                                                                                        |



 

 

 



