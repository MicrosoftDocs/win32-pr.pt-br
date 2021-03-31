---
title: Movendo usuários existentes para a unidade organizacional
description: Quando o administrador corporativo, Joe Worden, atualiza o domínio do Windows NT 4,0 para Active Directory, todos os usuários e grupos são migrados para os contêineres de usuários no domínio da Fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Movendo usuários existentes para o AD da unidade organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159294"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="f760d-104">Movendo usuários existentes para a unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="f760d-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="f760d-105">Quando o administrador corporativo, Joe Worden, atualiza o domínio do Windows NT 4,0 para Active Directory, todos os usuários e grupos são migrados para os contêineres de usuários no domínio da Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="f760d-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="f760d-106">Joe agora pode mover esses usuários e grupos para as unidades organizacionais apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f760d-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="f760d-107">Um objeto também pode ser movido entre domínios do Windows 2000 relacionados usando ADSI.</span><span class="sxs-lookup"><span data-stu-id="f760d-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="f760d-108">No exemplo de código a seguir, Joe move "jeffsmith" para a organização Sales.</span><span class="sxs-lookup"><span data-stu-id="f760d-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="f760d-109">O método [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) usa o ADsPath do objeto a ser movido e o nome do novo objeto (RDN).</span><span class="sxs-lookup"><span data-stu-id="f760d-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="f760d-110">Para manter o mesmo nome, você pode especificar **NULL** (**vbNullString**) para o parâmetro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="f760d-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="f760d-111">Para renomear o objeto quando ele for movido, especifique o novo nome distinto relativo para o parâmetro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="f760d-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="f760d-112">Por exemplo, para mover jeffsmith para a organização de vendas e renomear o objeto "jeffsmith" como "Jeff \_ Smith" na mesma operação, Joe executará o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="f760d-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="f760d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f760d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f760d-114">Criando novos usuários na unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="f760d-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




