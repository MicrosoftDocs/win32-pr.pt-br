---
title: Controle de acesso e criação de objeto
description: O servidor de Active Directory falhará ao criar um objeto filho se o chamador não tiver o \_ direito de \_ ADS \_ Create \_ filho para esse tipo de objeto no contêiner pai.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Controle de acesso e AD de criação de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b99251cd9c9c93177e0b6cfc362c7003078c870e809b48c9aba351e620e1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025719"
---
# <a name="access-control-and-object-creation"></a>Controle de acesso e criação de objeto

O servidor de Active Directory falhará ao criar um objeto filho se o chamador não tiver o **direito de ADS \_ \_ \_ Create \_ filho** para esse tipo de objeto no contêiner pai. Para determinar os tipos de objetos filho que o chamador pode criar em um objeto de diretório, leia o atributo **allowedChildClassesEffective** do objeto.

Quando você usa o método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para criar um objeto filho, o objeto não é tornado persistente até [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ser chamado no novo objeto. Entre as chamadas **Create** e **setinfo** , o thread de criação pode colocar valores em qualquer uma das propriedades do novo objeto. Após a chamada **setinfo** , o thread de criação não necessariamente tem os direitos de acesso para definir as propriedades do novo objeto. Para garantir que o chamador tenha esses direitos, especifique um descritor de segurança explícito durante a criação. A DACL deve ter uma ACE que concede ao chamador os direitos de acesso necessários no objeto.

Para obter mais informações sobre o controle de acesso e a criação de objetos, consulte [como descritores de segurança são definidos em novos objetos de diretório](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 