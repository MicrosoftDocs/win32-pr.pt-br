---
title: Recuperando a SACL de um objeto
description: O descritor de segurança de um objeto no Active Directory Domain Services pode conter uma SACL (lista de controle de acesso) do sistema.
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- AD SACL
- AD SACL, recuperando a SACL de um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293885"
---
# <a name="retrieving-an-objects-sacl"></a>Recuperando a SACL de um objeto

O descritor de segurança de um objeto no Active Directory Domain Services pode conter uma SACL (lista de controle de acesso) do sistema. Uma SACL contém ACEs (entradas de controle de acesso) que especificam os tipos de tentativas de acesso que geram registros de auditoria no log de eventos de segurança de um controlador de domínio. Lembre-se de que uma SACL gera entradas de log somente no controlador de domínio em que ocorreu a tentativa de acesso, não em cada DC que contém uma réplica do objeto.

Para definir ou obter a SACL de um descritor de segurança de objeto, o privilégio **\_ \_ nome de segurança se** deve ser habilitado no token de acesso do thread solicitante. O grupo Administradores tem esse privilégio por padrão e pode ser atribuído a outros usuários ou grupos. Para obter mais informações, consulte [direitos de acesso à SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Para obter e definir a SACL de um objeto de diretório, use a interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Usando C++, o método [**IADsSecurityDescriptor:: get \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) retorna um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) e use os métodos nessa interface para acessar as ACEs individuais na SACL. Para obter mais informações sobre o procedimento para modificar uma SACL, que é semelhante àquela para modificar uma DACL, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para enumerar as ACEs em uma SACL, use o método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) , que retorna um ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chame **QueryInterface** nesse ponteiro **IUnknown** para obter uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Use o método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar as ACEs na ACL. Cada ACE é retornado como uma **variante** que contém um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ; Lembre-se de que o membro **VT** é **\_ despacho VT**. Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para a Ace. Use os métodos de interface **IADsAccessControlEntry** para definir ou obter os componentes de uma ACE.

Para obter mais informações sobre as SACLs, consulte:

-   [Listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Geração de auditoria](/windows/desktop/SecAuthZ/audit-generation)

 

 