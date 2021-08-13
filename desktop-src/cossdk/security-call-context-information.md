---
description: Informações de contexto de chamada de segurança
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informações de contexto de chamada de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aed07f79fdba16f0ea6139a58cc50871d795e1eacbf94737b04dbf5f1fe900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546863"
---
# <a name="security-call-context-information"></a>Informações de contexto de chamada de segurança

A segurança baseada em função baseia-se em um mecanismo geral que permite recuperar informações de segurança sobre todos os chamadores upstream na cadeia de chamadas para seu componente. Essas informações só estarão disponíveis quando você tiver a verificação de função no nível do componente habilitada. Para obter detalhes sobre como definir a segurança no nível do componente, consulte [Definindo um nível de segurança para verificações de acesso.](setting-a-security-level-for-access-checks.md)

Você pode usar a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) para acessar informações de contexto de chamada de segurança programaticamente. Para uma descrição, consulte [Segurança de componente programático](programmatic-component-security.md).

O contexto de chamada de segurança é passado sempre que um limite de segurança é cruzado. Para chamadas entre componentes dentro de um aplicativo, que residem dentro do mesmo limite de segurança, nenhuma informação de contexto de chamada é passada. Para chamadas entre processos ou entre aplicativos dentro de um processo, chame fluxos de informações de contexto.

Esse recurso é particularmente útil se você quiser fazer auditoria e registro em log detalhados. Você pode recuperar e registrar informações de segurança para cada chamador upstream.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> <dt>

[Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



