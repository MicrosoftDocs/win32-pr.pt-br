---
title: Criando descritores de segurança para novos objetos de diretório
description: Você pode usar ADSI para criar um descritor de segurança e defini-lo como a propriedade nTSecurityDescriptor de um novo objeto ou usá-lo para substituir a propriedade nTSecurityDescriptor de um objeto existente.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Criando um descritor de segurança para um novo objeto de diretório AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453942"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Criando descritores de segurança para novos objetos de diretório

Você pode usar ADSI para criar um descritor de segurança e defini-lo como a propriedade **nTSecurityDescriptor** de um novo objeto ou usá-lo para substituir a propriedade **nTSecurityDescriptor** de um objeto existente.

Para criar um descritor de segurança para um objeto:

1.  Use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o objeto com ADSI para o novo descritor de segurança e obter um ponteiro de interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) para esse objeto. Lembre-se de que a ID de classe é **CLSID \_ SecurityDescriptor**.
2.  Use o método [**IADsSecurityDescriptor::p UT \_ Owner**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para definir o proprietário do objeto. O objeto de confiança é um usuário, grupo ou outra entidade de segurança. Um aplicativo deve usar o valor da propriedade apropriada do objeto user ou Group do Trustee ao qual aplicar a ACE.
3.  Use o método de [**\_ controle IADsSecurityDescriptor::p UT**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar se as DACLs e SACLs são herdadas pelo objeto de seu contêiner pai.
4.  Use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o objeto com ADSI para a DACL do novo descritor de segurança e obtenha um ponteiro de interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) para esse objeto. Lembre-se de que a ID de classe é **CLSID \_ AccessControlList**.
5.  Para cada ACE adicionar à DACL, use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o objeto com ADSI para a nova Ace e obter um ponteiro de interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para esse objeto. Lembre-se de que a ID de classe é CLSID \_ AccessControlEntry.
6.  Para cada ACE a adicionar à DACL, defina as propriedades da ACE usando os métodos de Propriedade do objeto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) da Ace. Para obter mais informações sobre as propriedades a serem definidas em uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).
7.  Para cada ACE a ser adicionada à DACL, use o método **QueryInterface** no objeto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para obter um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . O método [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) requer um ponteiro de interface **IDISPATCH** para a Ace.
8.  Para cada ACE a ser adicionada à DACL, use [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) para adicionar a nova Ace à DACL. Lembre-se de que a ordem das ACEs dentro da ACL pode afetar a avaliação do acesso ao objeto. O acesso correto ao objeto pode exigir que você crie uma nova ACL, adicione as ACEs da ACL existente na ordem correta à nova ACL e, em seguida, substitua a ACL existente no descritor de segurança pela nova ACL. Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Siga as etapas 4-8 para criar a SACL para o novo descritor de segurança.
10. Use o método [**IADsSecurityDescriptor::p UT \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para definir a DACL. Para obter mais informações sobre DACLs, consulte [DACLs nulas e DACLs vazias](null-dacls-and-empty-dacls.md).
11. Use o método [**IADsSecurityDescriptor::p UT \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para definir a SACL.
12. Converta o objeto [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) em uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) usando o método **QueryInterface** do objeto **IADsSecurityDescriptor** para obter uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Em seguida, defina o membro **VT** do **\_ despacho** **Variant** para VT e defina o membro **pdispVal** da **variante** igual ao ponteiro **IDispatch** .
13. Obtenha um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o objeto.
14. Use o método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) com "nTSecurityDescriptor" e a [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) criada acima para gravar o novo descritor de segurança no cache de propriedades.
15. Use o método [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para atualizar a propriedade no objeto no diretório.

 

 