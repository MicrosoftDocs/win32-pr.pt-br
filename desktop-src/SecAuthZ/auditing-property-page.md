---
description: O editor de controle de acesso pode incluir uma página de propriedades Auditoria que permite que o usuário veja e edite as ACEs (entradas de controle de acesso) em uma SACL (lista de controle de acesso do sistema) de objetos. Para obter mais informações sobre SACLs, consulte ACLs (Listas de Controle de Acesso).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Página de propriedades de auditoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf116a9079c5b7b6dfeb7e6df57b45d6a0a2555c14de88a32fee4fadcdc6373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784314"
---
# <a name="auditing-property-page"></a>Página de propriedades de auditoria

O editor de controle  de acesso pode incluir uma página de propriedades Auditoria que permite que o usuário veja e edite as ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) na SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema) de um objeto. Para obter mais informações sobre SACLs, consulte [ACLs](access-control-lists.md) (Listas de Controle de Acesso).

**Para exibir a página de propriedades Auditoria**

-   Na página [de propriedades básicas de segurança](basic-security-property-page.md), clique em **Avançado.** A **página de propriedades** Auditoria está na folha de propriedades de segurança [avançada](advanced-security-property-sheet.md).

Para incluir  a página de propriedades Auditoria, de definir os sinalizadores **SI \_ ADVANCED** e **SI \_ EDIT \_ AUDITS** na estrutura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação [**de ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)

 

 
