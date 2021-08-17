---
description: A seguir estão as classes COM+.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: COM+ Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2cdabc1f4535df6734cf525f288bf6cbd8a93543a9163848815441c9bc384c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129218"
---
# <a name="com-classes"></a>COM+ Classes

A seguir estão as classes COM+.



| Classe                                                            | Descrição                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appdomainhelper**](appdomainhelper.md)                       | Vincula um objeto gerenciado a um domínio de aplicativo, que é um ambiente isolado em que os aplicativos são executados.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Recupera informações sobre um assembly ao usar código gerenciado no .NET Framework Common Language Runtime.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Especifica e configura os serviços que devem estar ativos no domínio de serviço inserido ao chamar [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) ou [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).                     |
| [**Securitycallcontext**](securitycallcontext.md)               | Fornece acesso ao contexto de segurança da chamada atual, que contém informações sobre os chamadores de um objeto.                                                                                                                           |
| [**Securitycallers**](securitycallers.md)                       | Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores. A coleção representa a cadeia de chamadas que termina com a chamada atual e cada chamador na coleção representa a identidade de um chamador. |
| [**Securityidentity**](securityidentity.md)                     | Fornece acesso a uma coleção de informações de segurança que representam a identidade de um chamador. Usando essa classe, você pode descobrir sobre um chamador específico em uma cadeia de chamadores que faz parte do contexto de chamada de segurança.                 |
| [**Sharedproperty**](sharedproperty.md)                         | Define ou recupera o valor de uma propriedade compartilhada.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhadas.                                                                                                                                                                  |
| [**Sharedpropertygroupmanager**](sharedpropertygroupmanager.md) | Cria grupos de propriedades compartilhadas e para obter acesso a grupos de propriedades compartilhadas existentes.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Cria um objeto transacional genérico que inicia uma transação.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e fazer commit ou anular explicitamente a transação.        |



 

 

 



