---
description: Quando a segurança baseada em função está sendo usada, o objeto de contexto de chamada de segurança pode ser usado para acessar informações de segurança sobre a chamada atual.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Acessando informações de contexto de chamada de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164099"
---
# <a name="accessing-security-call-context-information"></a>Acessando informações de contexto de chamada de segurança

Quando a segurança baseada em função está sendo usada, o objeto de contexto de chamada de segurança pode ser usado para acessar informações de segurança sobre a chamada atual.

As seguintes coleções de propriedades estão disponíveis no objeto de contexto de chamada de segurança:

-   [Coleção SecurityCallContext](#securitycallcontext-collection)
-   [Coleção SecurityCallers](#securitycallers-collection)
-   [Coleção SecurityIdentity](#securityidentity-collection)
-   [Tópicos relacionados](#related-topics)

## <a name="securitycallcontext-collection"></a>Coleção SecurityCallContext



| Propriedade                          | Descrição                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | O número de chamadores na cadeia de chamadas.<br/>                                                                                |
| MinAuthenticationLevel<br/> | O nível de autenticação menos seguro de todos os chamadores na cadeia.<br/>                                                          |
| Chamadores<br/>                | Informações sobre a identidade dos chamadores upstream, na forma de uma coleção [**SecurityCallers**](securitycallers.md) .<br/> |
| DirectCaller<br/>           | O chamador que chamou o objeto diretamente (sem chamadores intermediários). <br/>                                                  |
| OriginalCaller<br/>         | O chamador que originou a cadeia de chamadas para o objeto. <br/>                                                               |



 

Para obter mais informações sobre como usar essa coleção, os desenvolvedores do Microsoft Visual Basic devem ver a classe [**SecurityCallContext**](securitycallcontext.md) . Os desenvolvedores de C e C++ devem se referir a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="securitycallers-collection"></a>Coleção SecurityCallers

A coleção [**SecurityCallers**](securitycallers.md) representa chamadores que podem ser recuperados usando um índice entre 0 e 1 menor que NumCallers, inclusive. Cada chamador é representado por um objeto [**SecurityIdentity**](securityidentity.md) .

Para obter mais informações sobre essa coleção, Visual Basic os desenvolvedores devem ver a classe [**SecurityCallers**](securitycallers.md) . Os desenvolvedores de C e C++ devem se referir a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>Coleção SecurityIdentity



| Propriedade                         | Descrição                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | O identificador de segurança do chamador.<br/>                                                                                                                   |
| AccountName<br/>           | O nome da conta do chamador.<br/>                                                                                                                           |
| AuthenticationService<br/> | O serviço de autenticação usado, como NTLMSSP, Kerberos ou SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | O nível de autenticação usado, que representa a quantidade de proteção usada ao se comunicar com o objeto.<br/>                                         |
| ImpersonationLevel<br/>    | O nível de representação definido pelo cliente, se a representação tiver sido usada. Esse nível indica a quantidade de autoridade atribuída ao servidor pelo cliente. <br/> |



 

Para obter mais informações sobre essa coleção, Visual Basic os desenvolvedores devem ver a classe [**SecurityIdentity**](securityidentity.md) . Os desenvolvedores de C e C++ devem se referir a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Verificando a associação de função](checking-role-membership.md)
</dt> <dt>

[Determinando se a segurança do Role-Based está habilitada](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> </dl>

 

 




