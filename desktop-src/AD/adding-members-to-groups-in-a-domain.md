---
title: Adicionando membros a grupos em um domínio
description: Este tópico mostra como adicionar membros a grupos em um domínio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Adicionando membros a grupos em um AD de domínio
- AD de grupos, adicionando membros a grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453963"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Adicionando membros a grupos em um domínio

Um grupo pode conter qualquer número de usuários, contatos ou outros grupos como membros. A lista a seguir lista os atributos do objeto de grupo que controlam a associação de grupo.



| Atributo                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**associado**](/windows/desktop/ADSchema/a-member)<br/>     | O atributo [**Member**](/windows/desktop/ADSchema/a-member) contém os nomes distintos para os objetos que são membros do grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | O atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) contém os nomes distintos dos grupos que contêm o grupo como um membro direto. O atributo **memberOf** não contém nenhum dado de associação de grupo herdado. Por exemplo, se GroupA for um membro de GroupB e GroupB for um membro de GroupC, o atributo **memberOf** do GroupA conterá GroupB, mas não GroupC.<br/> O servidor de Active Directory mantém essa propriedade. Quando um nome distinto é adicionado à propriedade [**Member**](/windows/desktop/ADSchema/a-member) de outro grupo, o nome diferenciado de outro grupo é adicionado à propriedade [**memberOf**](/windows/desktop/ADSchema/a-memberof) desse grupo.<br/> |



 

Cada um dos métodos a seguir pode ser usado para adicionar um membro a um grupo. Você pode adicionar um membro usando o nome distinto do membro ou ligando ao objeto member e, em seguida, adicionando o objeto member ao objeto Group.

Para adicionar um membro que pertence a um domínio de nível inferior a um grupo em um domínio de up-Level, use a forma vinculável da cadeia de caracteres de SID para o nome distinto. Para obter mais informações e um exemplo de código que mostra como converter um **objectSid** em uma cadeia de caracteres vinculável, consulte a função de exemplo **GetLDAPSidBindStringFromVariantSID** no [código de exemplo para converter um objectSid em uma cadeia de caracteres vinculável](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Adicionando membros a um grupo usando o IADs
</dt> <dd>

A interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) pode ser usada para adicionar membros a um grupo usando o método [**IADs. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Associar e obter a interface **IADs** para o objeto de grupo. Em seguida, o método **IADs. Add** pode ser usado para adicionar membros ao grupo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Adicionando membros a um grupo usando IDirectoryObject
</dt> <dd>

A interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pode ser usada para adicionar membros a um grupo usando o método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) para modificar o atributo de [**membro**](/windows/desktop/ADSchema/a-member) do grupo. Associar e obter a interface **IDirectoryObject** para o objeto de grupo. Em seguida, use o método **IDirectoryObject:: Setobjectattributes** para modificar o atributo de **membro** .

> [!Note]  
> Como o atributo de [**membro**](/windows/desktop/ADSchema/a-member) tem vários valores, certifique-se de usar o código de controle de **acréscimo de anúncios \_ \_ attr** para adicionar um nome distinto ao atributo de **membro** . Usar o código de controle de **\_ \_ atualização attr ADS** fará com que os valores de **membro** existentes sejam substituídos.

 

A interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) também pode ser usada para adicionar membros a um grupo quando o grupo é criado, especificando os membros no parâmetro *PAttributeEntries* do método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Adicionando membros a um grupo usando System. DirectoryServices
</dt> <dd>

Você pode usar o namespace [System. DirectoryServices](/dotnet/api/system.directoryservices) para adicionar membros a um grupo usando o método **PropertyValueCollection. Add** na propriedade **Member** do objeto Group. Para obter mais informações, consulte [definindo propriedades em objetos de diretório](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Adicionando membros a um grupo usando a API LDAP
</dt> <dd>

Você pode usar a API do [protocolo Lightweight Directory Access](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) para adicionar membros a um grupo usando uma das funções [**de \_ modificação \* de LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) . Para obter mais informações, consulte [modificando uma entrada de diretório](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

