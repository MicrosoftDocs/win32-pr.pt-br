---
title: Provedor LDAP ADSI
description: O provedor de LDAP ADSI implementa um conjunto de objetos ADSI que dão suporte a várias interfaces ADSI. Para acessar o provedor LDAP, associe-se a qualquer um dos objetos LDAP ADSI, usando o ADsPath LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Provedor LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822240"
---
# <a name="adsi-ldap-provider"></a>Provedor LDAP ADSI

O provedor de LDAP ADSI implementa um conjunto de objetos ADSI que dão suporte a várias interfaces ADSI. Para acessar o provedor LDAP, associe-se a qualquer um dos objetos LDAP ADSI, usando o ADsPath LDAP.

Você deve ter Adsldp.dll, Adsldpc.dll, Adsmsext.dll e Activeds.dll instalados no computador cliente para trabalhar com o provedor.

> [!Note]  
> O provedor LDAP ADSI padrão não pode ser considerado totalmente seguro para thread. Os gravadores de aplicativos multissegmentados devem coordenar corretamente o acesso entre os threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.

 

 

 




