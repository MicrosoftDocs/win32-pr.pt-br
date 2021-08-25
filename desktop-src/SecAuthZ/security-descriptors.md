---
description: Um descritor de segurança contém as informações de segurança associadas a um objeto seguro.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descritores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1049becf755bbb0940cfd5def3b59662a20eb2a690d90a36e06c5706212f02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907186"
---
# <a name="security-descriptors"></a>Descritores de segurança

Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) contém as informações de segurança associadas a um objeto [seguro](securable-objects.md). Um descritor de segurança consiste em uma estrutura [**\_ SECURITY DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e suas informações de segurança associadas. Um descritor de segurança pode incluir as seguintes informações de segurança:

-   [SIDs](security-identifiers.md) (identificadores de segurança) para o proprietário e o grupo primário de um objeto.
-   Uma [DACL](access-control-lists.md) que especifica os direitos de acesso permitidos ou negados a usuários ou grupos específicos.
-   Uma [SACL](access-control-lists.md) que especifica os tipos de tentativas de acesso que geram registros de auditoria para o objeto.
-   Um conjunto de bits de controle que qualificam o significado de um descritor de segurança ou seus membros individuais.

Os aplicativos não devem manipular diretamente o conteúdo de um descritor de segurança. A API Windows fornece funções para definir e recuperar as informações de segurança no descritor de segurança de um objeto. Além disso, há funções para criar e inicializar um descritor de segurança para um novo objeto.

Os aplicativos que trabalham com descritores de segurança em objetos do Active Directory podem usar as funções de segurança Windows ou as interfaces de segurança fornecidas pela ADSI (Interfaces de Serviço) do Active Directory. Para obter mais informações sobre interfaces de segurança ADSI, consulte [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
