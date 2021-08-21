---
title: Exclusão de controle de acesso e objeto
description: Active Directory permite que você exclua um objeto se tiver acesso de exclusão ao objeto ou aos anúncios \_ direito \_ DS \_ excluir \_ acesso filho ao tipo de objeto no contêiner pai.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Controle de acesso e AD de exclusão de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dda8f5eb241515e9428322ea01c6586b6870e7133e96a1cd7b4fcbb32f6f0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025631"
---
# <a name="access-control-and-object-deletion"></a>Exclusão de controle de acesso e objeto

Active Directory Domain Services permite que você exclua um objeto se tiver um dos seguintes direitos de acesso:

-   EXCLUIR o acesso ao próprio objeto
-   \_Direito \_ de ADS \_ excluir \_ acesso filho para esse tipo de objeto no contêiner pai

Lembre-se de que o sistema verifica o descritor de segurança para o objeto e seu pai antes de negar a exclusão. Isso significa que uma ACE que nega explicitamente o acesso de exclusão a um usuário não terá efeito se o usuário tiver excluir o \_ acesso filho no pai. Da mesma forma, uma ACE que nega \_ o acesso de exclusão filho no pai pode ser substituída se o acesso de exclusão for permitido no próprio objeto.

Para executar uma operação de exclusão de árvore, por exemplo, usando o método [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , você deve ter anúncios de \_ acesso à árvore de \_ exclusão DS do AD \_ \_ ao objeto. Se você tiver esse direito de acesso, poderá excluir o objeto e todos os objetos filho, independentemente das proteções nos objetos filho. Para excluir uma árvore se você não tiver anúncios \_ direito \_ \_ de excluir o DS de acesso à \_ árvore, será necessário percorrer recursivamente a árvore, excluindo cada objeto individualmente. Nesse caso, você deve ter o acesso de exclusão ou exclusão \_ de filho necessário para cada objeto na árvore.

> [!WARNING]
> Se os usuários tiverem \_ o ADS direito \_ \_ de excluir acesso à árvore do DS \_ para um objeto, isso lhes dará a capacidade de excluir uma subárvore inteira, incluindo todos os objetos filho. Por esse motivo, você pode considerar a revogação da permissão de acesso "Excluir Subárvore" para todos os usuários em um contêiner pai.

 

 

 