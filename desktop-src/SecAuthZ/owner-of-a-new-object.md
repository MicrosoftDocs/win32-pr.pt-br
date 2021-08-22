---
description: Um proprietário de objetos implicitamente tem \_ acesso de DAC de gravação ao objeto. Isso significa que o proprietário pode modificar a DACL (lista de controle de acesso discricionário) dos objetos e, portanto, pode controlar o acesso ao objeto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Proprietário de um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b787603e9225548e4213259866a6658d637bb85e46588f7260322fc2646128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912122"
---
# <a name="owner-of-a-new-object"></a>Proprietário de um novo objeto

O proprietário de um objeto implicitamente tem \_ acesso de DAC de gravação ao objeto. Isso significa que o proprietário pode modificar a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto e, portanto, pode controlar o acesso ao objeto.

O proprietário de um novo objeto é o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) padrão do proprietário do [*token de representação*](/windows/desktop/SecGloss/i-gly) ou [*primário*](/windows/desktop/SecGloss/p-gly) do [*processo*](/windows/desktop/SecGloss/p-gly)de criação. Para obter ou definir o proprietário padrão em um [*token de acesso*](/windows/desktop/SecGloss/a-gly), chame a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) com a estrutura de [**\_ proprietário do token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) . O sistema não permite que você defina o proprietário padrão de um token para um SID que não seja válido, como o SID da conta de outro usuário.

um processo com o \_ privilégio ES assumir \_ propriedade habilitado pode se definir como o proprietário de um objeto. um processo com o \_ privilégio ES restore \_ NAME habilitado ou com \_ acesso de proprietário de gravação ao objeto pode definir qualquer SID válido de usuário ou grupo como o proprietário de um objeto.

 

 
