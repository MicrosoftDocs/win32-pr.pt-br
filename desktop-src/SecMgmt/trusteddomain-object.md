---
description: O objeto TrustedDomain armazena informações sobre uma relação de confiança com um domínio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826978"
---
# <a name="trusteddomain-object"></a>Objeto TrustedDomain

O objeto **TrustedDomain** armazena informações sobre uma relação de confiança com um domínio. Um objeto **TrustedDomain** é criado no sistema confiante para identificar uma conta dentro do domínio confiável que pode ser usado para enviar solicitações de autenticação e para executar outras operações, como traduções de nome e Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ).

As informações armazenadas em um objeto **TrustedDomain** incluem:

-   O SID do domínio confiável. Essas informações não são modificáveis e devem ser exclusivas entre todos os objetos **TrustedDomain** .
-   O nome do domínio confiável. Essas informações não são modificáveis e devem ser exclusivas entre todos os objetos **TrustedDomain** .
-   O nome da conta no domínio confiável usado para enviar solicitações de autenticação e para executar traduções de nome e SID. Esse nome não é modificável.
-   A senha usada para enviar solicitações de autenticação e executar traduções de nome e SID.

Para obter mais informações, consulte [o tipo de objeto TrustedDomain](the-trusteddomain-object-type.md).

 

 
