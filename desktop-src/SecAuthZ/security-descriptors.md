---
description: Um descritor de segurança contém as informações de segurança associadas a um objeto protegível.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descritores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827333"
---
# <a name="security-descriptors"></a>Descritores de segurança

Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) contém as informações de segurança associadas a um [objeto protegível](securable-objects.md). Um descritor de segurança consiste em uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e suas informações de segurança associadas. Um descritor de segurança pode incluir as seguintes informações de segurança:

-   [Identificadores de segurança](security-identifiers.md) (SIDs) para o proprietário e o grupo primário de um objeto.
-   Uma [DACL](access-control-lists.md) que especifica os direitos de acesso permitidos ou negados a usuários ou grupos específicos.
-   Uma [SACL](access-control-lists.md) que especifica os tipos de tentativas de acesso que geram registros de auditoria para o objeto.
-   Um conjunto de bits de controle que qualifica o significado de um descritor de segurança ou seus membros individuais.

Os aplicativos não devem manipular diretamente o conteúdo de um descritor de segurança. A API do Windows fornece funções para configurar e recuperar as informações de segurança no descritor de segurança de um objeto. Além disso, há funções para criar e inicializar um descritor de segurança para um novo objeto.

Os aplicativos que trabalham com descritores de segurança em Active Directory objetos podem usar as funções de segurança do Windows ou as interfaces de segurança fornecidas pelas interfaces de serviço do Active Directory (ADSI). Para obter mais informações sobre as interfaces de segurança ADSI, consulte [como o controle de acesso funciona no Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
