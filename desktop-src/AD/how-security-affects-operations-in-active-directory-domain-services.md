---
title: Como a segurança afeta as operações no Active Directory Domain Services
description: Active Directory Domain Services usar o controle de acesso para conceder ou negar acesso a objetos, propriedades e operações com base na identidade do usuário que está executando a tentativa de acesso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Efeitos de segurança em Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8f5599afbc8552f9708fcfa953a069f429a152c4f0fff37546ffb7d9f6b809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188201"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Como a segurança afeta as operações no Active Directory Domain Services

Active Directory Domain Services usar o controle de acesso para conceder ou negar acesso a objetos, propriedades e operações com base na identidade do usuário que está executando a tentativa de acesso. Quando seu aplicativo é associado ao diretório, ele é associado a credenciais de usuário específicas. Quando autenticado, essas credenciais determinam o contexto de segurança do aplicativo. Independentemente de as credenciais serem aquelas do usuário conectado, um usuário especificado, uma conta de serviço, uma conta de computador ou um usuário não autenticado (convidado/todos), o servidor de Active Directory verifica o direito do usuário de acessar um objeto antes que qualquer operação seja executada nesse objeto. O usuário pode, ou não, ter acesso a um objeto específico, seus filhos, suas propriedades ou operações nesse objeto, o que significa que seu aplicativo deve lidar com os possíveis erros causados pelo acesso negado.

Para obter mais informações sobre contextos de segurança e os efeitos do controle de acesso em várias operações, consulte:

-   [Controle de acesso e operações de leitura](access-control-and-read-operations.md)
-   [Controle de acesso e operações de gravação](access-control-and-write-operations.md)
-   [Controle de acesso e criação de objeto](access-control-and-object-creation.md)
-   [Exclusão de controle de acesso e objeto](access-control-and-object-deletion.md)

 

 




