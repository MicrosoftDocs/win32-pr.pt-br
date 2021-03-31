---
title: Listas de controle de acesso para COM
description: Listas de controle de acesso para COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635489"
---
# <a name="access-control-lists-for-com"></a><span data-ttu-id="ecb88-103">Listas de controle de acesso para COM</span><span class="sxs-lookup"><span data-stu-id="ecb88-103">Access Control Lists for COM</span></span>

<span data-ttu-id="ecb88-104">O Windows Server XP Service Pack 2 (SP 2) e o Windows Server 2003 Service Pack 1 (SP 1) apresentam aprimoramentos de segurança para o Distributed Component Object Model (DCOM).</span><span class="sxs-lookup"><span data-stu-id="ecb88-104">Windows Server XP Service Pack 2 (SP 2) and Windows Server 2003 Service Pack 1 (SP 1) introduce security enhancements for the Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="ecb88-105">Um desses aprimoramentos é direitos de acesso mais específicos para uso em ACLs (listas de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="ecb88-105">One of these enhancements is more specific access rights for use in access control lists (ACLs).</span></span> <span data-ttu-id="ecb88-106">Os direitos de acesso são:</span><span class="sxs-lookup"><span data-stu-id="ecb88-106">The access rights are:</span></span>

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

<span data-ttu-id="ecb88-107">Para fornecer compatibilidade com versões anteriores, uma ACL pode existir no formato usado antes do Windows XP SP 2 e do Windows Server 2003 SP 1, que usa apenas o direito de acesso COM direitos de COM \_ \_ , ou pode existir no novo formato usado no Windows XP SP 2 e no windows Server 2003 SP 1, que usa os direitos com em \_ \_ execução junto com uma combinação de \_ direitos COM \_ \_ , executar direitos de COM e executar \_ \_ \_ remotamente, os direitos com são \_ \_ ativados \_ e os direitos com são \_ \_ ativados \_ remotamente.</span><span class="sxs-lookup"><span data-stu-id="ecb88-107">To provide backward compatibility, an ACL may exist in the format used before Windows XP SP 2 and Windows Server 2003 SP 1, which uses only the access right COM\_RIGHTS\_EXECUTE, or it may exist in the new format used in Windows XP SP 2 and Windows Server 2003 SP 1, which uses COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

> [!Note]  
> <span data-ttu-id="ecb88-108">\_Os direitos com são \_ executados sempre devem estar presentes; a ausência desse direito gera um descritor de segurança inválido.</span><span class="sxs-lookup"><span data-stu-id="ecb88-108">COM\_RIGHTS\_EXECUTE must always be present; the absence of this right generates an invalid security descriptor.</span></span>

 

<span data-ttu-id="ecb88-109">Você não deve misturar o formato antigo e o novo formato em uma única ACL; todas as ACEs (entradas de controle de acesso) devem conceder apenas o \_ direito de acesso de execução de direitos com \_ , ou todas elas devem conceder direitos com a serem \_ \_ executadas junto com uma combinação de direitos com, \_ executar direitos de com, executar \_ \_ \_ \_ \_ remotamente, \_ direitos com \_ \_ e direitos com \_ \_ Ativar \_ remotamente.</span><span class="sxs-lookup"><span data-stu-id="ecb88-109">You must not mix the old format and the new format within a single ACL; either all access control entries (ACEs) must grant only the COM\_RIGHTS\_EXECUTE access right, or they all must grant COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

<span data-ttu-id="ecb88-110">Veja a seguir um exemplo de uma ACL formatada incorretamente:</span><span class="sxs-lookup"><span data-stu-id="ecb88-110">The following is an example of an incorrectly formatted ACL:</span></span>

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

<span data-ttu-id="ecb88-111">Observe que a primeira entrada de controle de acesso (ACE) concede \_ somente os Rights \_ Execute (0x1), enquanto a segunda Ace concede a \_ \_ execução de direitos COM, \_ os direitos com são \_ executados \_ localmente, e os \_ direitos com \_ ativam \_ local (0xB) e o terceiro concede aos direitos com \_ e os direitos com \_ \_ \_ ativam \_ local (0x9).</span><span class="sxs-lookup"><span data-stu-id="ecb88-111">Note that the first access control entry (ACE) grants COM\_RIGHTS\_EXECUTE (0x1) only, while the second ACE grants COM\_RIGHTS\_EXECUTE, COM\_RIGHTS\_EXECUTE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_LOCAL (0xb), and the third grants COM\_RIGHTS\_EXECUTE and COM\_RIGHTS\_ACTIVATE\_LOCAL (0x9).</span></span>

<span data-ttu-id="ecb88-112">Para corrigir isso, a primeira ACE deve ser alterada para conceder que os direitos COM sejam \_ \_ executados em combinação com um dos outros quatro direitos de acesso, ou a segunda e a terceira ACEs devem ser alteradas para conceder somente direitos com de \_ \_ execução.</span><span class="sxs-lookup"><span data-stu-id="ecb88-112">To correct this, the first ACE should be changed to grant COM\_RIGHTS\_EXECUTE in combination with one of the other four access rights, or else the second and third ACEs should be changed to grant only COM\_RIGHTS\_EXECUTE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecb88-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecb88-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecb88-114">Aprimoramentos de segurança DCOM no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="ecb88-114">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[<span data-ttu-id="ecb88-115">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="ecb88-115">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




