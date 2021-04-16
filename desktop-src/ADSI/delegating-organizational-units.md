---
title: Delegando unidades organizacionais
description: A empresa Fabrikam contrata dois administradores, Mike e Paul, para gerenciar as unidades organizacionais leste e oeste, respectivamente.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754052"
---
# <a name="delegating-organizational-units"></a>Delegando unidades organizacionais

A empresa Fabrikam contrata dois administradores, Mike e Paul, para gerenciar as unidades organizacionais leste e oeste, respectivamente. Joe Delega suas responsabilidades administrativas a elas para que possam criar e excluir usuários em suas respectivas unidades organizacionais.

Antes de saber como configurar essas unidades organizacionais em Mike e Paul, você deve entender como configurar o acesso a objetos no Active Directory. Cada objeto no Active Directory tem um descritor de segurança. Com o descritor de segurança, você pode modificar permissões no objeto, propagar permissões, habilitar a auditoria e assim por diante. O descritor de segurança em si tem duas ACLs (listas de controle de acesso): uma DACL (ACL condicional) e uma SACL (ACL do sistema). Cada ACL pode conter ACEs (entradas de controle de acesso). Com uma ACE, você pode definir o acesso permitido ou negado em um objeto. Além disso, você pode especificar ações específicas para permitir ou negar. Exemplos de ações incluem criar filho, excluir filho, ler Propriedade e gravar propriedade. Esses direitos são especificados com [**AccessMask**](iadsaccesscontrolentry-property-methods.md).

Em seguida, você pode especificar as classes ou os atributos aos quais essa ACE está associada. No exemplo da Fabrikam a seguir, Joe escolhe a classe User para que cada administrador possa adicionar usuários ao sistema. Em seguida, você deve responder à pergunta: "quem será o beneficiário desta ACE?" Joe vai especificar Mike.

Por fim, você pode definir o comportamento de herança da ACE — por exemplo, as ACEs podem ser especificadas para propagar a hierarquia. Em resumo, o exemplo anterior fará com que Mike seja capaz de criar e excluir objetos de usuário na unidade organizacional vendas leste.

Joe usa o exemplo de código a seguir para configurar as ACEs e ACLs na unidade organizacional leste.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



A figura a seguir mostra o Active Directory menu **criar novo modo de exibição** após a execução do código. Quando Joe, o administrador, faz logon, ele vê várias classes que ele pode criar. No entanto, quando Mike fizer logon, ele só poderá criar objetos de usuário.

![menu de opção Criar novo modo de exibição](images/adadsi5.png)

Para obter mais informações, consulte [modelo de segurança ADSI](adsi-security-model.md).

 

 




