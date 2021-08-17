---
title: Adicionando membros a grupos em um domínio
description: Este tópico mostra como adicionar membros a grupos em um domínio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Adicionando membros a grupos em um AD de domínio
- Grupos do AD , adicionando membros a grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024753"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Adicionando membros a grupos em um domínio

Um grupo pode conter qualquer número de usuários, contatos ou outros grupos como membros. A lista a seguir lista os atributos do objeto de grupo que controlam a associação do grupo.



| Atributo                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Membro**](/windows/desktop/ADSchema/a-member)<br/>     | O [**atributo**](/windows/desktop/ADSchema/a-member) membro contém os nomes diferenciados para os objetos que são membros do grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Memberof**](/windows/desktop/ADSchema/a-memberof)<br/> | O [**atributo memberOf**](/windows/desktop/ADSchema/a-memberof) contém os nomes diferenciados de grupos que contêm o grupo como um membro direto. O **atributo memberOf** não contém nenhum dado de associação de grupo herdado. Por exemplo, se GroupA for membro de GroupB e GroupB for membro do GroupC, o atributo **memberOf** para GroupA conterá GroupB, mas não GroupC.<br/> O servidor do Active Directory mantém essa propriedade. Quando um nome diferenciado [](/windows/desktop/ADSchema/a-member) é adicionado à propriedade membro de outro grupo, o nome diferenciado de outro grupo é adicionado à [**propriedade memberOf desse**](/windows/desktop/ADSchema/a-memberof) grupo.<br/> |



 

Cada um dos métodos a seguir pode ser usado para adicionar um membro a um grupo. Você pode adicionar um membro usando o nome diferenciado do membro ou associação ao objeto membro e, em seguida, adicionando o objeto membro ao objeto de grupo.

Para adicionar um membro que pertence a um domínio de nível baixo a um grupo em um domínio de nível acima, use a forma a vinculo da cadeia de caracteres SID para o nome diferenciado. Para obter mais informações e um exemplo de código que mostra como converter **um objectSid** em uma cadeia de caracteres a vinculada, consulte a função de exemplo **GetLDAPSidBindStringFromVariantSID** em Código de Exemplo para Converter um [objectSid](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)em uma cadeia de caracteres a vincável .

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Adicionando membros a um grupo usando IADsGroup
</dt> <dd>

A [**interface IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) pode ser usada para adicionar membros a um grupo usando o [**método IADsGroup.Add.**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) Agrupe e obtenha a interface **IADsGroup** para o objeto de grupo. Em **seguida, o método IADsGroup.Add** pode ser usado para adicionar membros ao grupo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Adicionando membros a um grupo usando IDirectoryObject
</dt> <dd>

A interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pode ser usada para adicionar membros a um grupo usando o método [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) para modificar o atributo de membro do grupo. [](/windows/desktop/ADSchema/a-member) A bind a e obter a interface **IDirectoryObject** para o objeto de grupo. Em seguida, **use o método IDirectoryObject::SetObjectAttributes** para modificar o **atributo de** membro.

> [!Note]  
> Como o [**atributo de**](/windows/desktop/ADSchema/a-member) membro tem vários valores, use o código de controle **ADS \_ ATTR \_ APPEND** para adicionar um nome diferenciado ao **atributo de** membro. Usar o **código de controle ADS \_ ATTR \_ UPDATE** fará com que os valores de **membro** existentes sejam substituídos.

 

A interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) também pode ser usada para adicionar membros a um grupo quando o grupo é criado especificando os membros no parâmetro *pAttributeEntries* do método [**IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Adicionando membros a um grupo usando System.DirectoryServices
</dt> <dd>

Você pode usar o namespace [System.DirectoryServices](/dotnet/api/system.directoryservices) para adicionar membros a um grupo usando  o **método PropertyValueCollection.Add** na propriedade membro do objeto de grupo. Para obter mais informações, consulte [Configurando propriedades em objetos de diretório](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Adicionando membros a um grupo usando a API LDAP
</dt> <dd>

Você pode usar a API [lightweight directory access protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) para adicionar membros a um grupo usando uma das funções de [**\_ modificação \* ldap.**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) Para obter mais informações, consulte [Modificando uma entrada de diretório](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

