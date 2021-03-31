---
title: Exclusão de controle de acesso e objeto
description: Active Directory permite que você exclua um objeto se tiver acesso de exclusão ao objeto ou aos anúncios \_ direito \_ DS \_ excluir \_ acesso filho ao tipo de objeto no contêiner pai.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Controle de acesso e AD de exclusão de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640368"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="d7eea-104">Exclusão de controle de acesso e objeto</span><span class="sxs-lookup"><span data-stu-id="d7eea-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="d7eea-105">Active Directory Domain Services permite que você exclua um objeto se tiver um dos seguintes direitos de acesso:</span><span class="sxs-lookup"><span data-stu-id="d7eea-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="d7eea-106">EXCLUIR o acesso ao próprio objeto</span><span class="sxs-lookup"><span data-stu-id="d7eea-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="d7eea-107">\_Direito \_ de ADS \_ excluir \_ acesso filho para esse tipo de objeto no contêiner pai</span><span class="sxs-lookup"><span data-stu-id="d7eea-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="d7eea-108">Lembre-se de que o sistema verifica o descritor de segurança para o objeto e seu pai antes de negar a exclusão.</span><span class="sxs-lookup"><span data-stu-id="d7eea-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="d7eea-109">Isso significa que uma ACE que nega explicitamente o acesso de exclusão a um usuário não terá efeito se o usuário tiver excluir o \_ acesso filho no pai.</span><span class="sxs-lookup"><span data-stu-id="d7eea-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="d7eea-110">Da mesma forma, uma ACE que nega \_ o acesso de exclusão filho no pai pode ser substituída se o acesso de exclusão for permitido no próprio objeto.</span><span class="sxs-lookup"><span data-stu-id="d7eea-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="d7eea-111">Para executar uma operação de exclusão de árvore, por exemplo, usando o método [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , você deve ter anúncios de \_ acesso à árvore de \_ exclusão DS do AD \_ \_ ao objeto.</span><span class="sxs-lookup"><span data-stu-id="d7eea-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="d7eea-112">Se você tiver esse direito de acesso, poderá excluir o objeto e todos os objetos filho, independentemente das proteções nos objetos filho.</span><span class="sxs-lookup"><span data-stu-id="d7eea-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="d7eea-113">Para excluir uma árvore se você não tiver anúncios \_ direito \_ \_ de excluir o DS de acesso à \_ árvore, será necessário percorrer recursivamente a árvore, excluindo cada objeto individualmente.</span><span class="sxs-lookup"><span data-stu-id="d7eea-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="d7eea-114">Nesse caso, você deve ter o acesso de exclusão ou exclusão \_ de filho necessário para cada objeto na árvore.</span><span class="sxs-lookup"><span data-stu-id="d7eea-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="d7eea-115">Se os usuários tiverem \_ o ADS direito \_ \_ de excluir acesso à árvore do DS \_ para um objeto, isso lhes dará a capacidade de excluir uma subárvore inteira, incluindo todos os objetos filho.</span><span class="sxs-lookup"><span data-stu-id="d7eea-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="d7eea-116">Por esse motivo, você pode considerar a revogação da permissão de acesso "Excluir Subárvore" para todos os usuários em um contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="d7eea-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 