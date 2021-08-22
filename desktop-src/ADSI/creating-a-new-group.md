---
title: Criando um novo grupo
description: Joe Worden, administrador corporativo, deve criar um novo grupo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3f778e9eb953b60ca45665bcd92ff30efb9c111c959e78cf1824407d0a459c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962005"
---
# <a name="creating-a-new-group"></a>Criando um novo grupo

Joe Worden, administrador corporativo, deve criar um novo grupo. Ele gostaria de proteger alguns recursos, como arquivos, Active Directory objetos ou outros objetos, com base na associação desse grupo. O exemplo de código a seguir mostra como criar um novo grupo.


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



Esse grupo, gerenciamento, será criado na unidade organizacional Sales. Primeiro, Joe deve criar um objeto ADSI para a unidade organizacional Sales. Em segundo lugar, ele deve definir o atributo [**sAMAccountName**](/windows/desktop/AD/group-objects) nesse objeto, pois é um atributo obrigatório para compatibilidade com versões anteriores. para este exemplo, quando **samAccountName** é definido, Windows NT ferramentas 4,0 como o gerenciador de usuários confira o **atributo como gerenciamento, em** vez de **gerenciamento**.

Terceiro, Joe deve especificar o tipo de grupo. em um domínio Windows 2000, há três tipos de grupos: Global, domínio Local e Universal. Além disso, o grupo transporta sua característica de segurança. Um grupo pode ser um grupo habilitado para segurança ou não protegido. Essencialmente, os grupos habilitados para segurança são aqueles que podem ter direitos de acesso concedidos ou negados a recursos, semelhantes a um usuário. A concessão de um acesso de grupo a um compartilhamento de arquivos, por exemplo, implica que todos os membros do grupo podem acessar o compartilhamento de arquivos. As listas de distribuição não podem ser usadas de maneira semelhante — você não pode, por exemplo, conceder a uma lista de distribuição o direito de acessar um compartilhamento de arquivos. durante a atualização, Windows NT grupos de 4,0 são migrados como grupos habilitados para segurança. Os grupos não protegidos no Active Directory são semelhantes às listas de distribuição no Exchange. portanto, a criação de grupos ou listas de distribuição são operações semelhantes no Windows 2000. no modo nativo do Windows 2000 (modo nativo significa que todos os controladores de domínio em um domínio são computadores que executam Windows servidor 2000), os grupos podem ser aninhados em qualquer nível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerando objetos](enumerating-objects.md)
</dt> </dl>

 

 