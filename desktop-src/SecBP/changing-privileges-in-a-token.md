---
description: Explica como alterar privilégios em um token usando as funções AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Alterando privilégios em um token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771819"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="f3d12-103">Alterando privilégios em um token</span><span class="sxs-lookup"><span data-stu-id="f3d12-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="f3d12-104">Você pode alterar os privilégios de um token primário ou de representação de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="f3d12-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="f3d12-105">Habilite ou desabilite privilégios usando a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="f3d12-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="f3d12-106">Restrinja ou remova privilégios usando a função [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .</span><span class="sxs-lookup"><span data-stu-id="f3d12-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="f3d12-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) não pode adicionar ou remover privilégios do token.</span><span class="sxs-lookup"><span data-stu-id="f3d12-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="f3d12-108">Ele só pode habilitar os privilégios existentes atualmente desabilitados ou desabilitar os privilégios existentes que estão habilitados no momento.</span><span class="sxs-lookup"><span data-stu-id="f3d12-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="f3d12-109">Para obter exemplos, consulte [Habilitando e desabilitando privilégios em C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="f3d12-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="f3d12-110">Para atribuir privilégios a uma conta de usuário, consulte [atribuindo privilégios a uma conta](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="f3d12-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="f3d12-111">O [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) tem recursos mais abrangentes da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f3d12-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="f3d12-112">Removendo um privilégio.</span><span class="sxs-lookup"><span data-stu-id="f3d12-112">Removing a privilege.</span></span> <span data-ttu-id="f3d12-113">Observe que remover um privilégio não é o mesmo que desabilitar um.</span><span class="sxs-lookup"><span data-stu-id="f3d12-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="f3d12-114">Depois que um privilégio é removido de um token, ele não pode ser colocado de volta.</span><span class="sxs-lookup"><span data-stu-id="f3d12-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="f3d12-115">Anexando o atributo somente negação a SIDs no token.</span><span class="sxs-lookup"><span data-stu-id="f3d12-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="f3d12-116">Isso tem o efeito de não permitir contas ou grupos específicos, por exemplo, negar o acesso de exclusão de grupo Everyone a um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="f3d12-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="f3d12-117">Para obter mais informações sobre como restringir SIDs, consulte [atributos de Sid em um token de acesso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="f3d12-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="f3d12-118">Especificar uma lista de SIDs de restrição no token.</span><span class="sxs-lookup"><span data-stu-id="f3d12-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="f3d12-119">Para obter informações sobre como restringir SIDs, consulte [tokens restritos](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="f3d12-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
