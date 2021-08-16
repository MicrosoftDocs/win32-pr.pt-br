---
title: Listas de controle de acesso para COM
description: Listas de controle de acesso para COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50e1641691b1a2812e861a95c5bc0f7eac8f0f8af67d41b18287c07253b8d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551350"
---
# <a name="access-control-lists-for-com"></a>Listas de controle de acesso para COM

Windows O Server XP Service Pack 2 (SP 2) e o Windows Server 2003 Service Pack 1 (SP 1) introduzem aprimoramentos de segurança para o DCOM (Distributed Component Object Model). Um desses aprimoramentos são direitos de acesso mais específicos para uso em ACLs (listas de controle de acesso). Os direitos de acesso são:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Para fornecer compatibilidade com compatibilidade com backward, Uma ACL pode existir no formato usado antes do Windows XP SP 2 e do Windows Server 2003 SP 1, que usa apenas o direito de acesso COM RIGHTS EXECUTE ou pode existir no novo formato usado no Windows XP SP 2 e \_ no Windows Server 2003 SP 1, que usa COM RIGHTS EXECUTE junto com uma combinação de \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL e \_ COM RIGHTS \_ ACTIVATE \_ \_ \_ \_ \_ \_ \_ REMOTE.

> [!Note]  
> COM RIGHTS EXECUTE sempre deve estar presente; a ausência desse \_ direito gera um \_ descritor de segurança inválido.

 

Você não deve misturar o formato antigo e o novo formato em uma única ACL; todas as ACEs (entradas de controle de acesso) devem conceder apenas o direito de acesso COM RIGHTS EXECUTE ou todas elas devem conceder DIREITOS COM EXECUTE junto com uma combinação de \_ \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL e \_ COM RIGHTS \_ ACTIVATE \_ \_ \_ \_ \_ \_ \_ REMOTE.

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

Observe que a primeira ace (entrada de controle de acesso) concede somente COM RIGHTS EXECUTE (0x1), enquanto a segunda ACE concede COM RIGHTS EXECUTE, COM RIGHTS EXECUTE LOCAL e COM RIGHTS ACTIVATE LOCAL (0xb) e o terceiro concede DIREITOS COM EXECUTE e \_ \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ LOCAL \_ \_ \_ \_ \_ \_ \_ \_ \_ (0x9).

Para corrigir isso, a primeira ACE deve ser alterada para conceder DIREITOS COM EXECUTE em combinação com um dos outros quatro direitos de acesso, caso contrário, o segundo e o terceiro ACEs devem ser alterados para conceder apenas \_ \_ COM RIGHTS \_ \_ EXECUTE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de segurança do DCOM no Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




