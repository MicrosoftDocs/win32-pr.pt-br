---
title: Criando um usuário
description: Para criar um usuário no Active Directory Domain Services, crie um objeto de usuário no contêiner de domínio do domínio em que você deseja colocar o usuário.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, criando um usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea10d0142af650d58b61967b008b207abca2c11
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824029"
---
# <a name="creating-a-user"></a>Criando um usuário

Para criar um usuário no Active Directory Domain Services, crie um objeto de usuário no contêiner de domínio do domínio em que você deseja colocar o usuário. Os usuários podem ser criados na raiz do domínio, em uma unidade organizacional ou em um contêiner.

Ao criar um objeto de usuário, você também deve definir os atributos, listados na tabela a seguir, para definir o objeto como um usuário legal reconhecido pelo Active Directory Domain Services e pelo sistema de segurança do Windows.



| Atributo                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cn**](/windows/desktop/ADSchema/a-cn)                         | Especifica o nome do objeto de usuário no diretório. Esse será o RDN (nome distinto relativo) do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Especifica uma cadeia de caracteres que é o nome usado para dar suporte a clientes e servidores de uma versão anterior do Windows. O [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve ter menos de 20 caracteres para dar suporte a clientes de uma versão anterior do Windows.<br/> O [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve ser exclusivo entre todos os objetos de entidade de segurança no domínio. Você deve executar uma consulta em relação ao domínio para verificar se **sAMAccountName** é exclusivo dentro do domínio.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) é um atributo opcional. O servidor criará um valor **sAMAccountName** aleatório se nenhum for especificado.<br/> |



 

Você também pode definir outros atributos. Os seguintes atributos de usuário serão definidos com valores padrão se você não defini-los explicitamente no momento da criação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a></td>
<td>Especifica quando a conta vai expirar. O padrão é <strong>TIMEQ_FOREVER</strong>, que indica que a conta nunca expirará.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a></td>
<td>Um descritor de segurança é criado com base em regras específicas. Para obter mais informações, consulte <a href="how-security-descriptors-are-set-on-new-directory-objects.md">como descritores de segurança são definidos em novos objetos de diretório</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a></td>
<td>Especifica a categoria de usuário. O padrão é &quot; Person &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-name"><strong>nomes</strong></a></td>
<td>Especifica um nome de usuário. O padrão é o valor definido para <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a></td>
<td>Especifica quando o usuário definiu a senha pela última vez. O padrão é zero, que indica que o usuário deve alterar a senha no próximo logon.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a></td>
<td>Contém valores que determinam vários recursos de logon e conta para o usuário.<br/> Por padrão, os seguintes sinalizadores são definidos:<br/>
<ul>
<li><strong>UF_ACCOUNTDISABLE</strong> - A conta está desabilitada.</li>
<li><strong>UF_PASSWD_NOTREQD</strong> - Nenhuma senha é necessária.</li>
<li><strong>UF_NORMAL_ACCOUNT</strong> - Tipo de conta padrão que representa um usuário típico.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a></td>
<td>Especifica o grupo ou grupos dos quais o usuário é um membro direto. O padrão é &quot; usuários do domínio &quot; .<br/></td>
</tr>
</tbody>
</table>



 

Um usuário é criado ligando-se ao contêiner desejado e, em seguida, usando um dos métodos a seguir. Os atributos [**CN**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) devem ser definidos antes que o usuário seja confirmado no servidor.



| Método                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | O atributo [**CN**](/windows/desktop/ADSchema/a-cn) é extraído do parâmetro *bstrRelativeName* . O novo usuário deve ser confirmado chamando [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ou o objeto não será criado. Para obter mais informações, consulte [código de exemplo para criar um usuário](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | O atributo [**CN**](/windows/desktop/ADSchema/a-cn) é extraído do parâmetro *pszRDNName* . O novo usuário é confirmado quando [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) é chamado. Para obter mais informações, consulte [código de exemplo para criar um usuário](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [DirectoryEntries. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | O atributo [**CN**](/windows/desktop/ADSchema/a-cn) é obtido do parâmetro *Name* . O novo objeto de usuário deve ser confirmado chamando [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) ou o objeto não será criado. Para obter mais informações, consulte [adicionando objetos de diretório](/previous-versions/ms180851(v=vs.90)).<br/> |



 

O novo usuário deve ser confirmado no servidor antes que qualquer atributo diferente de [**CN**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) possa ser modificado. Isso ocorre porque a conta de usuário não existe de fato até que o usuário seja confirmado. Se um atributo for recuperado ou modificado para um objeto que não existe no servidor, ocorrerá um erro. Isso inclui chamar o método [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Por exemplo, a sequência a seguir seria seguida ao criar um usuário com [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Chame [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para criar o usuário no cache local com o [**CN**](/windows/desktop/ADSchema/a-cn)especificado.
2.  Defina o atributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) para o valor desejado com o método [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) .
3.  Agora, modifique outros atributos, como [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Essa restrição também se aplica às propriedades ADSI, como [**IADsUser. AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods), e métodos como [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Chame [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar o novo usuário no servidor.

Quando uma nova conta de usuário é criada, ela é desabilitada por padrão. A conta deve ser habilitada manualmente ou programaticamente. Para habilitar programaticamente uma conta de usuário, remova o sinalizador **ADS \_ UF \_ ACCOUNTDISABLE** do atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

Quando uma nova conta de usuário é criada, o atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) da conta automaticamente tem o sinalizador da **UF \_ passwd \_ NOTREQD** definido, o que indica que nenhuma senha é necessária para a conta. Se as políticas de segurança do domínio em que a conta é criada exigirem uma senha para todas as contas de usuário, o sinalizador **UF \_ passwd \_ NOTREQD** deverá ser removido do atributo **userAccountControl** para a conta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de código para criar um usuário](example-code-for-creating-a-user.md)
</dt> </dl>