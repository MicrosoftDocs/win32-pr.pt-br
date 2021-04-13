---
description: A API da AuthZ permite que os aplicativos executem verificações de acesso personalizáveis com melhor desempenho e desenvolvimento mais simplificado do que o controle de acesso de baixo nível.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Usando a API AuthZ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297590"
---
# <a name="using-authz-api"></a>Usando a API AuthZ

A API da AuthZ permite que os aplicativos executem verificações de acesso personalizáveis com melhor desempenho e desenvolvimento mais simplificado do que o [controle de acesso de baixo nível](low-level-access-control.md).

A API da AuthZ permite que os aplicativos armazenem em cache as verificações de desempenho para obter um aumento de performance, consultar e modificar contextos do cliente e definir regras de negócio que possam ser usadas para avaliar a permissão de acesso dinamicamente.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                             | Descrição                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializando um contexto de cliente](initializing-a-client-context.md)<br/>     | Um aplicativo deve criar um contexto de cliente antes de poder usar a API AuthZ para executar verificações de acesso ou auditoria.<br/>                                                                                                                                            |
| [Consultando um contexto de cliente](querying-a-client-context.md)<br/>             | Os aplicativos podem chamar a função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar informações sobre um contexto de cliente existente.<br/>                                                                                       |
| [Adicionando SIDs a um contexto de cliente](adding-sids-to-a-client-context.md)<br/> | Um aplicativo pode adicionar SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) a um contexto de cliente existente chamando a função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .<br/> |
| [Verificando o acesso com a API AuthZ](checking-access-with-authz-api.md)<br/>   | Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .<br/>                                                                                                                |
| [Cache de verificações de acesso](caching-access-checks.md)<br/>                     | Quando um aplicativo executa uma verificação de acesso chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , os resultados dessa verificação de acesso podem ser armazenados em cache.<br/>                                                                                       |



 

 

