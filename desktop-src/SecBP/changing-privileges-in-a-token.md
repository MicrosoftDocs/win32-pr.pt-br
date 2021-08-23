---
description: Explica como alterar privilégios em um token usando as funções AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Alterando privilégios em um token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622746"
---
# <a name="changing-privileges-in-a-token"></a>Alterando privilégios em um token

Você pode alterar os privilégios de um token primário ou de representação de duas maneiras:

-   Habilite ou desabilite privilégios usando a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .
-   Restrinja ou remova privilégios usando a função [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) não pode adicionar ou remover privilégios do token. Ele só pode habilitar os privilégios existentes atualmente desabilitados ou desabilitar os privilégios existentes que estão habilitados no momento. Para obter exemplos, consulte [Habilitando e desabilitando privilégios em C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Para atribuir privilégios a uma conta de usuário, consulte [atribuindo privilégios a uma conta](assigning-privileges-to-an-account.md).

O [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) tem recursos mais abrangentes da seguinte maneira:

-   Removendo um privilégio. Observe que remover um privilégio não é o mesmo que desabilitar um. Depois que um privilégio é removido de um token, ele não pode ser colocado de volta.
-   Anexando o atributo somente negação a SIDs no token. Isso tem o efeito de não permitir contas ou grupos específicos, por exemplo, negar o acesso de exclusão de grupo Everyone a um arquivo específico. Para obter mais informações sobre como restringir SIDs, consulte [atributos de Sid em um token de acesso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Especificar uma lista de SIDs de restrição no token. Para obter informações sobre como restringir SIDs, consulte [tokens restritos](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
