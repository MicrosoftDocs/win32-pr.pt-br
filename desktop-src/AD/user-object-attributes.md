---
title: Atributos de objeto de usuário
description: Um objeto de usuário tem vários atributos. Esta seção documenta os principais atributos usados por Windows, ferramentas administrativas e o WAB (Windows Catálogo de Endereços). Ele não descreve todos os atributos; muitos atributos não são usados para o objeto de usuário.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- AD de atributos de objeto de usuário
- AD de usuários, atributos de objeto de usuário
- Objetos AD , Usuário, Atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1bb6b347bd55daceb07dfe1fad4adc3e1352afc91ec14018aab6b24615c2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182625"
---
# <a name="user-object-attributes"></a>Atributos de objeto de usuário

Um objeto de usuário tem vários atributos. Esta seção documenta os principais atributos usados por Windows, ferramentas administrativas e o WAB (Windows Catálogo de Endereços). Ele não descreve todos os atributos; muitos atributos não são usados para o objeto de usuário.

Alguns atributos são armazenados no diretório, como [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor,**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)e assim por diante, e replicados para todos os controladores de domínio em um domínio. Um subconjunto desses atributos também é replicado para o catálogo global.

Atributos não replicados são armazenados em cada controlador de domínio, mas não são replicados em outro lugar, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon,**](/windows/desktop/ADSchema/a-lastlogon) [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)e assim por diante. Os atributos não replicados são atributos que pertencem a um controlador de domínio específico. Por exemplo, **lastLogon** é a última data e hora em que o logon de rede do usuário foi validado pelo controlador de domínio específico que está retornando a propriedade.

Um objeto de usuário também tem atributos construídos que não são armazenados no diretório, mas são calculados pelo controlador de domínio, como [**canonicalName,**](/windows/desktop/ADSchema/a-canonicalname) [**distinguishedName,**](/windows/desktop/ADSchema/a-distinguishedname) [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)e assim por diante.

Atributos para objetos de usuário são classificados como:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Atributos de objeto base
</dt> <dd>

Essa categoria inclui atributos necessários para todos os objetos de diretório, como [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e assim por diante.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Atributos de nomeação
</dt> <dd>

Essa categoria inclui atributos usados para se referir ou identificar o objeto, como [**distinguishedName,**](/windows/desktop/ADSchema/a-distinguishedname) [**objectGUID,**](/windows/desktop/ADSchema/a-objectguid) [**objectSID**](/windows/desktop/ADSchema/a-objectsid)e assim por diante. Para obter mais informações sobre como nomear atributos para objetos de usuário, consulte [Atributos de nomen por nome de usuário.](naming-properties.md)

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Atributos de segurança
</dt> <dd>

Essa categoria inclui atributos para logon e controle de acesso. Para obter mais informações sobre atributos de segurança para objetos de usuário, consulte [Atributos de segurança do usuário.](security-properties.md)

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Catálogo de Endereços atributos
</dt> <dd>

Essa categoria inclui atributos para dados de email e usuário. Para obter mais informações sobre atributos do livro de endereços para objetos de usuário, consulte [Atributos Catálogo de Endereços usuário](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Atributos específicos do aplicativo
</dt> <dd>

Essa categoria inclui dados de configuração específicos do usuário para aplicativos específicos.

</dd> </dl>

Para obter mais informações sobre como ler e modificar atributos para um objeto de usuário, consulte Lendo e escrevendo atributos de objetos [no Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Para obter mais informações sobre a classe User, incluindo uma lista completa dos [**atributos mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) da classe , consulte [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Configurando senhas

A senha de um usuário não pode ser modificada diretamente porque isso envolveria o envio de uma senha não criptografada pela rede. Para definir a senha de um usuário, é necessário usar o método [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) ou [**IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) O **método IADsUser.ChangePassword** é usado quando o aplicativo está permitindo que o usuário altere sua própria senha. O **método IADsUser.SetPassword** é usado quando o aplicativo permite que um administrador redefina uma senha.

 

 