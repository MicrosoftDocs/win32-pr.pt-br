---
description: Explica como alterar privilégios em um token usando as funções AdjustTokenPrivileges e CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Alterando privilégios em um token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771819"
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

 

 
