---
title: Recuperando a DACL de um objeto
description: O descritor de segurança de um objeto pode conter uma DACL (lista de controle de acesso discricionário).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- ANÚNCIO DACL
- O AD DACL, recuperando a DACL de um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025104"
---
# <a name="retrieving-an-objects-dacl"></a>Recuperando a DACL de um objeto

O descritor de segurança de um objeto pode conter uma DACL (lista de controle de acesso discricionário). Uma DACL contém zero ou mais ACEs (entradas de controle de acesso) que identificam os usuários e grupos que podem acessar o objeto. Se uma DACL estiver vazia (ou seja, ela contiver zero ACEs), nenhum acesso será explicitamente concedido, portanto o acesso será negado implicitamente. No entanto, se o descritor de segurança de um objeto não tiver uma DACL, o objeto será desprotegido e todos terão acesso completo.

Para recuperar a DACL de um objeto, você deve ser o proprietário do objeto ou ter acesso de **\_ controle de leitura** ao objeto.

Para obter e definir a DACL de um objeto de diretório, use a interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Usando C++, o método [**IADsSecurityDescriptor:: get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) retorna um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) e use os métodos nessa interface para acessar as ACEs individuais na DACL. O procedimento para modificar uma DACL é descrito em [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para enumerar as ACEs, use o método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) . O método retorna um ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chame **QueryInterface** nesse ponteiro **IUnknown** para obter uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Use o método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar as ACEs na ACL. Cada ACE é retornado como uma **variante** que contém um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (  o membro VT **é \_ despacho VT**). Chame **QueryInterface** nesse ponteiro **IDispatch** para obter uma interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para a Ace. Você pode usar os métodos da interface **IADsAccessControlEntry** para definir ou recuperar os componentes de uma ACE.

Para obter mais informações sobre DACLs e ACEs, consulte os tópicos a seguir no Platform Software Development Kit (SDK).

-   [Listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
-   [ACEs (entradas de controle de acesso)](/windows/desktop/SecAuthZ/access-control-entries)

 

 