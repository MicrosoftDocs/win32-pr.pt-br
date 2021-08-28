---
description: Torna as interfaces da API de script para o WMI disponíveis para programadores C/C++, no lugar das versões da API COM.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Interfaces de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c05c1682513e0c0a0d76d88990e80bcc8e6e2d22767ea6fced6f1facca59119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820286"
---
# <a name="automation-interfaces"></a>Interfaces de automação

A API de automação torna as interfaces da API de script para o WMI disponíveis para programadores C/C++, no lugar das versões da API COM.

A tabela a seguir lista os objetos WMI e como eles são usados na API de automação. O link de referências cruzadas para a documentação da interface da API de script para equivalentes do WMI.



| Objeto Automation                                 | Descrição                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | Recupera eventos em conjunto com [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).   |
| [**ISWbemLastError**](swbemlasterror.md)         | Fornece informações de erro estendidas quando ocorre um erro.                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | Obtém uma referência a um objeto [**ISWbemServices**](swbemservices.md) que pode acessar o WMI em um computador host específico. |
| [**ISWbemMethod**](swbemmethod.md)               | Contém uma única definição de método.                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | Obtém acesso a uma coleção de objetos [**ISWbemMethod**](swbemmethod.md) .                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | Contém um único valor nomeado.                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | Obtém acesso a uma coleção de objetos [**ISWbemNamedValue**](swbemnamedvalue.md) .                                         |
| [**ISWbemObject**](swbemobject.md)               | Contém e manipula uma única classe ou instância de objeto de modelo CIM (CIM).                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | Gera e valida um caminho de objeto.                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | Obtém acesso a uma coleção de objetos [**ISWbemObject**](swbemobject.md) .                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | Define ou limpa um privilégio.                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | Obtém acesso a uma coleção de objetos [**ISWbemPrivilege**](swbemprivilege.md) .                                           |
| [**ISWbemProperty**](swbemproperty.md)           | Usado para conter uma única propriedade CIM.                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | Obter acesso a uma coleção de objetos [**ISWbemProperty**](swbemproperty.md) .                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | Contém um qualificador de classe única.                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | Obtém acesso a uma coleção de objetos [**ISWbemQualifier**](swbemqualifier.md) .                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | Gerencia configurações de segurança, como privilégio de Component Object Model (COM), AuthenticationLevel e ImpersonationLevel.      |
| [**ISWbemServices**](swbemservices.md)           | Cria, atualiza e recupera instâncias ou classes.                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | Recebe os resultados de operações assíncronas de aplicativo cliente e notificações de eventos.                                 |



 

 

 



