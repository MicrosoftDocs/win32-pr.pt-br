---
title: Criando novos usuários na unidade organizacional
description: Terry Adams foi contratado na organização de vendas da Fabrikam. Seu relatório direto é Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Criando novos usuários na unidade organizacional ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453487"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Criando novos usuários na unidade organizacional

Terry Adams foi contratado na organização de vendas da Fabrikam. Seu relatório direto é Patrick Hines.

Conforme mostrado no exemplo de código a seguir, Joe Andreshak, administrador corporativo, criará uma nova conta para ele.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



Ao criar um novo usuário, você deve especificar um **sAMAccountName**. Este é um atributo obrigatório para a classe User. Antes que uma instância de um objeto possa ser criada, todos os atributos obrigatórios devem ser definidos. O **sAMAccountName** será gerado automaticamente se um não for especificado para um novo usuário.

Ao criar um novo usuário, todos os atributos necessários devem ser definidos no cache local antes que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.

Joe, como administrador, pode atribuir a senha de Terry usando o método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) . O método **IADsUser. SetPassword** não funcionará até que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tenha sido chamado.

Em seguida, Joe habilita a conta de usuário definindo a propriedade [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) como **false**.

O exemplo de código a seguir mostra como definir Terry como gerente do Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Você pode estar imaginando o que acontece se Terry alterar seu nome, mudar para uma organização diferente ou deixar a empresa. Quem mantém este link de relatório direto do gerente? Para obter mais informações e a solução para esse problema, consulte [reorganização](reorganization.md). Como o esquema de Active Directory é extensível, você pode modelar seus objetos para incluir relações de estilo de relatório diretas de gerentes semelhantes.

Antes de prosseguir para a próxima tarefa, veja um exemplo de código que mostra como Joe exibirá os subordinados diretos de Terry.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



Neste exemplo de código, Patrick será exibido como o relatório direto de Terry, embora o atributo **DirectReports** nunca tenha sido modificado. Active Directory faz isso automaticamente.

No mundo do diretório, um atributo pode ter um ou vários valores. Como **DirectReports** tem vários valores, você pode obter essas informações examinando o esquema, é mais fácil usar o método [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , que retorna uma matriz de valores, independentemente de os valores únicos ou múltiplos serem retornados.

O snap-in Active Directory usuários e computadores permite exibir relatórios diretos e relações de gerente na página de propriedades do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Adicionando usuários a um grupo](adding-users-to-a-group.md)
</dt> </dl>

 

 




