---
description: O editor de controle de acesso pode incluir uma página de propriedades de auditoria que permite ao usuário exibir e editar as ACEs (entradas de controle de acesso) em uma SACL (lista de controle de acesso) do sistema de objetos. Para obter mais informações sobre as SACLs, consulte listas de controle de acesso (ACLs).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Página de propriedades de auditoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170407"
---
# <a name="auditing-property-page"></a>Página de propriedades de auditoria

O editor de controle de acesso pode incluir uma página de propriedades de **auditoria** que permite ao usuário exibir e editar as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na SACL (lista de controle de acesso) do [*sistema*](/windows/desktop/SecGloss/s-gly) de um objeto. Para obter mais informações sobre as SACLs, consulte [listas de controle de acesso](access-control-lists.md) (ACLs).

**Para exibir a página de propriedades de auditoria**

-   Na [página de propriedades segurança básica](basic-security-property-page.md), clique em **avançado**. A página de propriedades de **auditoria** está na [folha de propriedades segurança avançada](advanced-security-property-sheet.md).

Para incluir a página de propriedades de **auditoria** , defina os sinalizadores de **\_ \_ auditoria** **si \_ avançado** e si editar na estrutura de [**\_ \_ informações do objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
