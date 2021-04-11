---
description: Informações de contexto de chamada de segurança
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informações de contexto de chamada de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164158"
---
# <a name="security-call-context-information"></a>Informações de contexto de chamada de segurança

A segurança baseada em funções é criada em um mecanismo geral que permite que você recupere informações de segurança sobre todos os chamadores upstream na cadeia de chamadas para seu componente. Essas informações estão disponíveis somente quando você tem a verificação de função no nível de componente habilitada. Para obter detalhes sobre como definir a segurança em nível de componente, consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).

Você pode usar a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) para acessar informações de contexto de chamada de segurança programaticamente. Para obter uma descrição, consulte [segurança de componente programática](programmatic-component-security.md).

O contexto de chamada de segurança é passado sempre que um limite de segurança é ultrapassado. Para chamadas entre componentes dentro de um aplicativo, que residem no mesmo limite de segurança, nenhuma informação de contexto de chamada é passada. Para chamadas entre processos ou entre aplicativos em um processo, os fluxos de informações de contexto de chamada.

Esse recurso será particularmente útil se você quiser fazer auditoria e log detalhados. Você pode recuperar e registrar informações de segurança para cada chamador upstream.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Propriedade de contexto de segurança](security-context-property.md)
</dt> <dt>

[Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



