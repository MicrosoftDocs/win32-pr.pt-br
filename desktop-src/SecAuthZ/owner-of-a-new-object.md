---
description: Um proprietário de objetos implicitamente tem \_ acesso de DAC de gravação ao objeto. Isso significa que o proprietário pode modificar a DACL (lista de controle de acesso discricionário) dos objetos e, portanto, pode controlar o acesso ao objeto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Proprietário de um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756384"
---
# <a name="owner-of-a-new-object"></a>Proprietário de um novo objeto

O proprietário de um objeto implicitamente tem \_ acesso de DAC de gravação ao objeto. Isso significa que o proprietário pode modificar a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto e, portanto, pode controlar o acesso ao objeto.

O proprietário de um novo objeto é o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) padrão do proprietário do [*token de representação*](/windows/desktop/SecGloss/i-gly) ou [*primário*](/windows/desktop/SecGloss/p-gly) do [*processo*](/windows/desktop/SecGloss/p-gly)de criação. Para obter ou definir o proprietário padrão em um [*token de acesso*](/windows/desktop/SecGloss/a-gly), chame a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) com a estrutura de [**\_ proprietário do token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) . O sistema não permite que você defina o proprietário padrão de um token para um SID que não seja válido, como o SID da conta de outro usuário.

Um processo com o \_ privilégio se assumir \_ propriedade habilitado pode se definir como o proprietário de um objeto. Um processo com o \_ privilégio do nome de restauração se \_ habilitado ou com acesso de proprietário de gravação \_ ao objeto pode definir qualquer Sid válido de usuário ou grupo como o proprietário de um objeto.

 

 
