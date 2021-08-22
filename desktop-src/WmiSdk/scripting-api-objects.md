---
description: A referência da API de Script para WMI descreve cada objeto de script usando uma sintaxe específica. Para uma explicação dessa sintaxe, consulte Convenções de documento para a API de Script.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Objetos de API de script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd639e1b1ca482a2b1aa95a4e0a6a26672480660440af290c043814ce5f8e965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050304"
---
# <a name="scripting-api-objects"></a>Objetos de API de script

A referência da API de Script para WMI descreve cada objeto de script usando uma sintaxe específica. Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

A tabela a seguir lista objetos de script WMI e como eles são usados.



| Objeto                                               | Descrição                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Constrói e analisado valores [datetime](date-and-time-format.md) cim.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Recupera eventos em conjunto com [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Fornece informações de erro estendidas quando ocorre um erro.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Obtém um [**objeto SWbemServices**](swbemservices.md) que pode obter acesso ao WMI em um computador host específico.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contém uma única definição de método WMI.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Obtém uma coleção de [**objetos SWbemMethod.**](swbemmethod.md)                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contém um único valor nomeado.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Obtém acesso a uma coleção de [**objetos SWbemNamedValue.**](swbemnamedvalue.md)                                                                                                                                                                     |
| [**Swbemobject**](swbemobject.md)                   | Contém e manipula uma única instância ou classe de objeto WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Estende a funcionalidade de [**SWbemObject.**](swbemobject.md) Esse objeto adiciona o [**método Refresh**](swbemrefresher-refresh.md) para [**objetos SWbemRefresher.**](swbemrefresher.md)                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Gera e valida um caminho de objeto.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Obtém acesso a uma coleção de [**objetos SWbemObject.**](swbemobject.md)                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Define ou limpa um privilégio.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Obtém acesso a uma coleção de [**objetos SWbemPrivilege.**](swbemprivilege.md)                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Contém uma única propriedade WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Obtém acesso a uma coleção de [**objetos SWbemProperty.**](swbemproperty.md)                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Contém um qualificador de propriedade única.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Obtém acesso a uma coleção de [**objetos SWbemQualifier.**](swbemqualifier.md)                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Coleta e atualiza valores de propriedade de objeto em uma operação.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Representa um único elemento atualizável em um [**objeto SWbemRefresher,**](swbemrefresher.md) como uma propriedade .                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Gerencia configurações de segurança, como privilégios [](swbemsecurity-privileges.md)Component Object Model (COM), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)e [**ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)   |
| [**SWbemServices**](swbemservices.md)               | Cria, atualiza e recupera instâncias ou classes.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Estende a funcionalidade de [**SWbemServices.**](swbemservices.md) Esse objeto adiciona os [**métodos Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) para permitir que uma classe ou instância seja salva em vários namespaces. |
| [**SWbemSink**](swbemsink.md)                       | Recebe os resultados de operações assíncronas e notificações de eventos, que são usadas por aplicativos cliente.                                                                                                                                        |



 

 

 



