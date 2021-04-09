---
description: A seguir estão as classes COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: Classes COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089697"
---
# <a name="com-classes"></a>Classes COM+

A seguir estão as classes COM+.



| Classe                                                            | Descrição                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Associa um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera informações sobre um assembly ao usar código gerenciado no Common Language Runtime de .NET Framework.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Especifica e configura os serviços que devem estar ativos no domínio de serviço inserido ao chamar [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) ou [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Fornece acesso ao contexto de segurança da chamada atual, que contém informações sobre os chamadores de um objeto.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores. A coleção representa a cadeia de chamadas terminando com a chamada atual, e cada chamador na coleção representa a identidade de um chamador. |
| [**SecurityIdentity**](securityidentity.md)                     | Fornece acesso a uma coleção de informações de segurança que representa a identidade de um chamador. Usando essa classe, você pode descobrir sobre um determinado chamador em uma cadeia de chamadores que faz parte do contexto de chamada de segurança.                 |
| [**SharedProperty**](sharedproperty.md)                         | Define ou recupera o valor de uma propriedade compartilhada.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhado.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Cria grupos de propriedades compartilhadas e obtém acesso a grupos de propriedades compartilhadas existentes.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Cria um objeto transacional genérico que inicia uma transação.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.        |



 

 

 



