---
title: Segurança de partição do Diretório do Aplicativo
description: O modelo de controle de acesso e segurança para partições de diretório de aplicativo é o mesmo para outras partições no Active Directory Domain Services.
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- AD de Segurança da Partição do Diretório do Aplicativo
- Partições do diretório de aplicativos AD , Segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20da5f0c869329637ae6182224cf67e2feb5684491c34534ac80a67f72b795c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024396"
---
# <a name="application-directory-partition-security"></a>Segurança de partição do Diretório do Aplicativo

O modelo de controle de acesso e segurança para partições de diretório de aplicativo é o mesmo para outras partições no Active Directory Domain Services. Os usuários normais podem acessar objetos em uma partição de diretório do aplicativo sujeitos às ACLs colocadas nesses objetos. Para obter mais informações, consulte [Controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

No entanto, como as partições de diretório do aplicativo podem abranger vários domínios de segurança em um serviço de diretório, surge a pergunta de como interpretar constantes de cadeia de caracteres SID conhecidas relativas ao domínio no [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) da classe de esquema de um objeto no momento da criação do objeto em uma partição de diretório de aplicativo. Por exemplo, se "DA" se referir ao grupo de administradores de domínio, mas em uma partição de diretório do aplicativo, não será conhecido a qual domínio o grupo "DA" se refere.

Para resolver esse problema, o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) de uma partição de diretório de aplicativo tem um atributo [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) que contém o nome diferenciado do domínio de referência para essa partição de diretório do aplicativo. O sistema de segurança usa o domínio especificado para interpretar referências de domínio local para descritores de segurança padrão anexados a objetos criados nessa partição de diretório do aplicativo. O domínio de referência pode ser especificado quando o **objeto crossRef** para uma partição de diretório do aplicativo é criado. Isso requer, no entanto, que um **objeto crossRef** seja pré-criado para a partição de diretório do aplicativo. Se nenhum domínio de referência for especificado, o sistema define automaticamente o domínio de referência com base em uma das seguintes condições:

-   Se o pai do objeto de partição de diretório do aplicativo for outra partição de diretório de aplicativo, o atributo [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) da partição de diretório do aplicativo pai será usado para o domínio de referência.
-   Se o objeto pai for um domínio, esse domínio será usado para o domínio de referência.
-   Se não houver nenhum objeto pai, o domínio raiz da floresta será usado para o domínio de referência.

O **atributo crossRef** também pode ser alterado para o domínio de referência depois que a partição é criada, mas isso não é recomendado.

Um problema semelhante ocorrerá se um grupo local for especificado em uma ACL para um objeto em uma partição de diretório do aplicativo. Nesse caso, o [**atributo msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) não pode ser usado para interpretar o domínio de referência para um grupo local. Para evitar esse problema, os grupos locais não devem ser usados nas ACLs dos objetos de partição do diretório do aplicativo.

 

 