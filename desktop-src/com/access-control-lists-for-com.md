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
# <a name="access-control-lists-for-com"></a>Listas de controle de acesso para COM

O Windows Server XP Service Pack 2 (SP 2) e o Windows Server 2003 Service Pack 1 (SP 1) apresentam aprimoramentos de segurança para o Distributed Component Object Model (DCOM). Um desses aprimoramentos é direitos de acesso mais específicos para uso em ACLs (listas de controle de acesso). Os direitos de acesso são:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Para fornecer compatibilidade com versões anteriores, uma ACL pode existir no formato usado antes do Windows XP SP 2 e do Windows Server 2003 SP 1, que usa apenas o direito de acesso COM direitos de COM \_ \_ , ou pode existir no novo formato usado no Windows XP SP 2 e no windows Server 2003 SP 1, que usa os direitos com em \_ \_ execução junto com uma combinação de \_ direitos COM \_ \_ , executar direitos de COM e executar \_ \_ \_ remotamente, os direitos com são \_ \_ ativados \_ e os direitos com são \_ \_ ativados \_ remotamente.

> [!Note]  
> \_Os direitos com são \_ executados sempre devem estar presentes; a ausência desse direito gera um descritor de segurança inválido.

 

Você não deve misturar o formato antigo e o novo formato em uma única ACL; todas as ACEs (entradas de controle de acesso) devem conceder apenas o \_ direito de acesso de execução de direitos com \_ , ou todas elas devem conceder direitos com a serem \_ \_ executadas junto com uma combinação de direitos com, \_ executar direitos de com, executar \_ \_ \_ \_ \_ remotamente, \_ direitos com \_ \_ e direitos com \_ \_ Ativar \_ remotamente.

Veja a seguir um exemplo de uma ACL formatada incorretamente:

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

Observe que a primeira entrada de controle de acesso (ACE) concede \_ somente os Rights \_ Execute (0x1), enquanto a segunda Ace concede a \_ \_ execução de direitos COM, \_ os direitos com são \_ executados \_ localmente, e os \_ direitos com \_ ativam \_ local (0xB) e o terceiro concede aos direitos com \_ e os direitos com \_ \_ \_ ativam \_ local (0x9).

Para corrigir isso, a primeira ACE deve ser alterada para conceder que os direitos COM sejam \_ \_ executados em combinação com um dos outros quatro direitos de acesso, ou a segunda e a terceira ACEs devem ser alteradas para conceder somente direitos com de \_ \_ execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de segurança DCOM no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




