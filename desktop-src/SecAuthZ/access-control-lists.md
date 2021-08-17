---
description: Uma lista de controle de acesso (ACL) é uma lista de entradas de controle de acesso (ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Listas de Controle de Acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7021767830dead84f2ea965c46ca205257a2f18443f352ec85becc0139e30e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785656"
---
# <a name="access-control-lists"></a>Listas de Controle de Acesso

Uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) é uma lista de entradas de controle de [acesso](access-control-entries.md) (ACE). Cada ACE em uma ACL identifica [um objeto de confiança](trustees.md) e especifica [os direitos de acesso](access-rights-and-access-masks.md) permitidos, negados ou auditados para esse objeto de confiança. O [descritor de segurança](security-descriptors.md) para um [objeto protegível](securable-objects.md) pode conter dois tipos de ACLs: uma DACL e uma SACL.

Uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) identifica os confiáveis que têm permissão ou acesso negado a um objeto protegível. Quando um [*processo*](/windows/desktop/SecGloss/p-gly) tenta acessar um objeto protegível, o sistema verifica as ACEs na DACL do objeto para determinar se deve conceder acesso a ela. Se o objeto não tiver uma DACL, o sistema concederá acesso completo a todos. Se a DACL do objeto não tiver ACEs, o sistema negará todas as tentativas de acessar o objeto porque a DACL não permite nenhum direito de acesso. O sistema verifica as ACEs em sequência até encontrar uma ou mais ACEs que permitem todos os direitos de acesso solicitados ou até que qualquer um dos direitos de acesso solicitados seja negado. Para obter mais informações, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md). Para obter informações sobre como criar uma DACL corretamente, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

Uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema permite que os administradores registrem tentativas de acessar um objeto protegido. Cada ACE especifica os tipos de tentativas de acesso por um confiável especificado que fazem com que o sistema gere um registro no log de eventos de segurança. Uma ACE em uma SACL pode gerar registros de auditoria quando uma tentativa de acesso falhar, quando for bem-sucedida, ou ambos. Para obter mais informações sobre as SACLs, consulte a [geração de auditoria](audit-generation.md) e o [direito de acesso à SACL](sacl-access-right.md).

Não tente trabalhar diretamente com o conteúdo de uma ACL. Para garantir que as ACLs estejam semanticamente corretas, use as funções apropriadas para criar e manipular ACLs. Para obter mais informações, consulte [obtendo informações de uma ACL](getting-information-from-an-acl.md) e [criando ou modificando uma ACL](creating-or-modifying-an-acl.md).

As ACLs também fornecem controle de acesso aos objetos do serviço de diretório do Microsoft Active Directory. As interfaces de serviço do Active Directory (ADSI) incluem rotinas para criar e modificar o conteúdo dessas ACLs. Para obter mais informações, consulte [controlando o acesso a objetos de Active Directory](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services).

 

 
