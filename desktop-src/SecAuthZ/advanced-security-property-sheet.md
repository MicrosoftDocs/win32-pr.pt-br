---
description: A folha de propriedades segurança avançada permite que o usuário execute operações de edição que não estão disponíveis na página de propriedades de segurança básica de um editor de controle de acesso.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Folha de propriedades de segurança avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752134"
---
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="ade94-103">Folha de propriedades de segurança avançada</span><span class="sxs-lookup"><span data-stu-id="ade94-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="ade94-104">A folha de propriedades segurança avançada permite que o usuário execute operações de edição que não estão disponíveis na [página de propriedades de segurança básica](basic-security-property-page.md) de um editor de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="ade94-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="ade94-105">A folha de propriedades pode incluir as seguintes páginas de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ade94-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="ade94-106">Uma página de propriedades de [permissões](permissions-property-page.md) para edição avançada da DACL [*(lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto, como editar [ACEs específicas do objeto](object-specific-aces.md) ou controlar a herança da [Ace](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="ade94-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="ade94-107">Uma página de propriedades de [auditoria](auditing-property-page.md) para exibir e editar a SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema do objeto.</span><span class="sxs-lookup"><span data-stu-id="ade94-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="ade94-108">Uma página de propriedades do [proprietário](owner-property-page.md) para alterar o proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="ade94-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="ade94-109">O usuário pode exibir a folha de propriedades segurança avançada clicando no botão **avançado** na página de propriedades de segurança básica.</span><span class="sxs-lookup"><span data-stu-id="ade94-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="ade94-110">Para exibir o botão **avançado** , defina o \_ sinalizador avançado de si na estrutura de [**\_ \_ informações do objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="ade94-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
