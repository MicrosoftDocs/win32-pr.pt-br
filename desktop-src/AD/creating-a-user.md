---
title: Criando um usuário
description: Para criar um usuário no Active Directory Domain Services, crie um objeto de usuário no contêiner de domínio do domínio em que você deseja colocar o usuário.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Exemplos do Active Directory do Active Directory, criando um usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469223"
---
# <a name="creating-a-user"></a>Criando um usuário

Para criar um usuário no Active Directory Domain Services, crie um objeto de usuário no contêiner de domínio do domínio em que você deseja colocar o usuário. Os usuários podem ser criados na raiz do domínio, em uma unidade organizacional ou em um contêiner.

Ao criar um objeto de usuário, você também deve definir os atributos, listados na tabela a seguir, para definir o objeto como um usuário legal que é reconhecido pelo Active Directory Domain Services e pelo sistema Segurança do Windows.



| Atributo                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cn**](/windows/desktop/ADSchema/a-cn)                         | Especifica o nome do objeto de usuário no diretório. Esse será o RDN (nome diferenciado relativo) do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname) | Especifica uma cadeia de caracteres que é o nome usado para dar suporte a clientes e servidores de uma versão anterior do Windows. O [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve ter menos de 20 caracteres para dar suporte a clientes de uma versão anterior do Windows.<br/> O [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve ser exclusivo entre todos os objetos de entidade de segurança dentro do domínio. Você deve executar uma consulta no domínio para verificar se **o sAMAccountName** é exclusivo dentro do domínio.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) é um atributo opcional. O servidor criará um valor **sAMAccountName** aleatório se nenhum for especificado.<br/> |



 

Você também pode definir outros atributos. Os atributos de usuário a seguir serão definidos com valores padrão se você não defini-los explicitamente no momento da criação.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a> | Especifica quando a conta expirará. O padrão é <strong>TIMEQ_FOREVER</strong>, que indica que a conta nunca expirará.<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>Ntsecuritydescriptor</strong></a> | Um descritor de segurança é criado com base em regras específicas. Para obter mais informações, consulte <a href="how-security-descriptors-are-set-on-new-directory-objects.md">How Security Descriptors are Set on New Directory Objects</a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | Especifica a categoria de usuário. O padrão é "Pessoa".<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>Nome</strong></a> | Especifica um nome de usuário. O padrão é o valor definido para <a href="/windows/desktop/ADSchema/a-cn"><strong>cn.</strong></a><br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | Especifica quando o usuário definiu a senha pela última vez. O padrão é zero, o que indica que o usuário deve alterar a senha no próximo logon.<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | Contém valores que determinam vários recursos de logon e conta para o usuário.<br /> Por padrão, os seguintes sinalizadores são definidos:<br /><ul><li><strong>UF_ACCOUNTDISABLE</strong> - a conta está desabilitada.</li><li><strong>UF_PASSWD_NOTREQD</strong> - nenhuma senha é necessária.</li><li><strong>UF_NORMAL_ACCOUNT</strong> - Tipo de conta padrão que representa um usuário típico.</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a> | Especifica o grupo ou grupos dos que o usuário é um membro direto. O padrão é "Usuários do Domínio".<br /> | 




 

Um usuário é criado pela associação ao contêiner desejado e, em seguida, usando um dos métodos a seguir. Os [**atributos cn**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) devem ser definidos antes que o usuário seja confirmado no servidor.



| Método                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | O [**atributo cn**](/windows/desktop/ADSchema/a-cn) é retirado do parâmetro *bstrRelativeName.* O novo usuário deve ser confirmado chamando [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ou o objeto não será criado. Para obter mais informações, consulte [Código de exemplo para criar um usuário.](example-code-for-creating-a-user.md)<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | O [**atributo cn**](/windows/desktop/ADSchema/a-cn) é retirado do parâmetro *pszRDNName.* O novo usuário é comprometido quando [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) é chamado. Para obter mais informações, consulte [Código de exemplo para criar um usuário.](example-code-for-creating-a-user.md)<br/>                                                                                                                |
| [DirectoryEntries.Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | O [**atributo cn**](/windows/desktop/ADSchema/a-cn) é retirado do parâmetro *name.* O novo objeto de usuário deve ser confirmado chamando [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) ou o objeto não será criado. Para obter mais informações, consulte [Adicionando objetos de diretório](/previous-versions/ms180851(v=vs.90)).<br/> |



 

O novo usuário deve ser confirmado no servidor antes que quaisquer atributos que não [**sejam cn**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) possam ser modificados. Isso acontece porque a conta de usuário não existe até que o usuário seja comprometido. Se um atributo for recuperado ou modificado para um objeto que não existe no servidor, ocorrerá um erro. Isso inclui chamar o [**método IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) Por exemplo, a sequência a seguir seria seguida ao criar um usuário com [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Chame [**IADsContainer.Create para**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) criar o usuário no cache local com o [**cn especificado.**](/windows/desktop/ADSchema/a-cn)
2.  De definir [**o atributo sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) como o valor desejado com o [**método IADs.Put.**](/windows/desktop/api/iads/nf-iads-iads-put)
3.  Agora, modifique outros atributos, como [**userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) Essa restrição também se aplica às propriedades ADSI, como [**IADsUser.AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods)e métodos como [**IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword)
4.  Chame [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para fazer commit do novo usuário no servidor.

Quando uma nova conta de usuário é criada, ela é desabilitada por padrão. A conta deve ser habilitada manual ou programaticamente. Para habilitar programaticamente uma conta de usuário, remova o sinalizador **\_ ADS UF \_ ACCOUNTDISABLE** do [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

Quando uma nova conta de usuário é criada, o atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) para a conta tem automaticamente o **sinalizador \_ \_ NOTREQD DAL PASSWD** definido, o que indica que nenhuma senha é necessária para a conta. Se as políticas de segurança do domínio em que a conta é criada exigirem uma senha para todas as contas de usuário, o sinalizador **\_ \_ NOTREQD DALV PASSWD** deverá ser removido do **atributo userAccountControl** da conta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo para criar um usuário](example-code-for-creating-a-user.md)
</dt> </dl>
