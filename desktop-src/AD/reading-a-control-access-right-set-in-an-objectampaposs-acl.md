---
title: Lendo um conjunto direito de acesso de controle na ACL de um objeto
description: As propriedades da interface IADsAccessControlEntry são usadas para conceder ou negar direitos de acesso de controle.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Lendo um conjunto direito de acesso de controle na ACL de um objeto Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007299"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Lendo um conjunto direito de acesso de controle na ACL de um objeto

Usando o ADSI, você lê um ACE de acesso de controle da mesma forma como faria com qualquer outra ACE em uma ACL. Lembre-se de que você também pode usar as APIs de segurança do Win32 para ler ACLs em objetos de diretório. No entanto, os direitos de acesso de controle usam as propriedades da interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) de uma maneira específica para conceder e negar direitos de acesso de controle:

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) deve conter **anúncios \_ direito \_ de \_ \_ acesso de controle DS**.
-   O valor dos [**sinalizadores**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é **tipo de \_ objeto sinalizador ADS \_ \_ \_ presente**.
-   [**Objecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é a forma de cadeia de caracteres do atributo **rightsGUID** do direito de acesso de controle. O formato da cadeia de caracteres do GUID é o mesmo formato de cadeia de caracteres que a função de biblioteca com [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) .
-   O [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é **o \_ \_ objeto de \_ acesso \_ permitido pelo ADS AceType** para conceder o objeto de acesso de controle de confiança do direito ou do **ADS \_ AceType \_ acesso \_ negado \_** para negar o direito de acesso de controle de confiança.
-   [**Trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) é a entidade de segurança; Esse é o usuário, o grupo, o computador e assim por diante, ao qual a ACE se aplica.

Use o procedimento a seguir para ler uma ACE para um objeto ADSI. O procedimento a seguir se aplica a aplicativos C e C++.

**Para ler uma ACE para um objeto ADSI**

1.  Obtenha um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o objeto.
2.  Use o método [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obter o descritor de segurança do objeto. O nome da propriedade que contém o descritor de segurança é "nTSecurityDescriptor". A propriedade será retornada como uma **variante** que contém um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Lembre-se de que o membro **VT** é **\_ despacho VT**. Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) para usar os métodos nessa interface para acessar a ACL do descritor de segurança.
3.  Use o método [**IADsSecurityDescriptor:: get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para obter a ACL. O método retorna um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) para usar os métodos nessa interface para acessar as ACEs individuais na ACL.
4.  Use o método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) para enumerar as ACEs. O método retorna um ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chame **QueryInterface** nesse ponteiro **IUnknown** para obter uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .
5.  Use o método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar as ACEs na ACL. A propriedade é retornada como uma **variante** que contém um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Lembre-se de que o membro **VT** é **\_ despacho VT**. Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para ler a Ace.
6.  Chame o [**método IADsAccessControlEntry:: \_ Get AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obter a **AccessMask** e verifique se o valor de **AccessMask** para o sinalizador de **\_ \_ \_ \_ acesso de controle DS direito ADS** . Se tiver esse sinalizador, a ACE conterá um direito de acesso de controle.
7.  Chame o método de [**\_ sinalizadores IADsAccessControlEntry:: Get**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obter o sinalizador para o tipo de objeto.
8.  Marque o valor dos [**sinalizadores**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para o sinalizador do **tipo de \_ objeto sinalizador do ADS \_ \_ \_ presente** . Se **sinalizadores** estiverem definidos para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**, chame o método **IADsAccessControlEntry:: get \_ objecttype** para obter uma cadeia de caracteres que contenha o rightsGUID do direito de acesso de controle ao qual a Ace se aplica.
9.  Chame o método [**IADsAccessControlEntry:: get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obter o tipo ACE. O tipo será um **\_ \_ \_ \_ objeto permitido pelo ADS ACETYPE Access** para conceder o objeto de acesso de controle de confiança ao direito ou aos **anúncios \_ ACETYPE \_ acesso \_ negado \_** para negar o direito de acesso de controle.
10. Chame o método [**IADsAccessControlEntry:: Get de \_ Trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obter a entidade de segurança; ou seja, User, Group, Computer e assim por diante ao qual a Ace se aplica.
11. Quando terminar com as cadeias de caracteres [**objecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **Trustee** , use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória para essas cadeias de caracteres.
12. Quando terminar com as interfaces, chame **Release** para decrementar ou libere todas as referências de interface.

 

 