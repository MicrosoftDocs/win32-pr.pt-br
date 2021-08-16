---
description: O editor de controle de acesso pode incluir uma página de propriedades de auditoria que permite ao usuário exibir e editar as ACEs (entradas de controle de acesso) em uma SACL (lista de controle de acesso) do sistema de objetos. Para obter mais informações sobre as SACLs, consulte listas de controle de acesso (ACLs).
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

O editor de controle de acesso pode incluir uma página de propriedades de **auditoria** que permite ao usuário exibir e editar as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na SACL (lista de controle de acesso) do [*sistema*](/windows/desktop/SecGloss/s-gly) de um objeto. Para obter mais informações sobre as SACLs, consulte [listas de controle de acesso](access-control-lists.md) (ACLs).

**Para exibir a página de propriedades de auditoria**

-   Na [página de propriedades segurança básica](basic-security-property-page.md), clique em **avançado**. A página de propriedades de **auditoria** está na [folha de propriedades segurança avançada](advanced-security-property-sheet.md).

Para incluir a página de propriedades de **auditoria** , defina os sinalizadores de **\_ \_ auditoria** **si \_ avançado** e si editar na estrutura de [**\_ \_ informações do objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
