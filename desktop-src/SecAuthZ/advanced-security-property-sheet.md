---
description: A folha de propriedades segurança avançada permite que o usuário execute operações de edição que não estão disponíveis na página de propriedades de segurança básica de um editor de controle de acesso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Folha de propriedades de segurança avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808eaefaa481e828504eb55b3ecc3b70d487c03af82b296c3b8bc02da2b354d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914342"
---
# <a name="advanced-security-property-sheet"></a>Folha de propriedades de segurança avançada

A folha de propriedades segurança avançada permite que o usuário execute operações de edição que não estão disponíveis na [página de propriedades de segurança básica](basic-security-property-page.md) de um editor de controle de acesso. A folha de propriedades pode incluir as seguintes páginas de propriedades:

-   Uma página de propriedades de [permissões](permissions-property-page.md) para edição avançada da DACL [*(lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto, como editar [ACEs específicas do objeto](object-specific-aces.md) ou controlar a herança da [Ace](ace-inheritance.md).
-   Uma página de propriedades de [auditoria](auditing-property-page.md) para exibir e editar a SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema do objeto.
-   Uma página de propriedades do [proprietário](owner-property-page.md) para alterar o proprietário do objeto.

O usuário pode exibir a folha de propriedades segurança avançada clicando no botão **avançado** na página de propriedades de segurança básica. Para exibir o botão **avançado** , defina o \_ sinalizador avançado de si na estrutura de [**\_ \_ informações do objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
