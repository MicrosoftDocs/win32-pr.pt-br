---
description: Define um perfil de banda larga móvel.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Referência de esquema de perfil de banda larga móvel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783217"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Referência de esquema de perfil de banda larga móvel

O esquema de perfil de banda larga móvel define um perfil de banda larga móvel.

Os perfis armazenam parâmetros de configuração de rede e de usuário relacionados à conexão de banda larga móvel. Eles também armazenam as preferências do usuário para uma conexão.

O elemento raiz de um perfil de banda larga móvel é o elemento [**MBNProfile**](schema-mbnprofile-element.md) . Cada perfil tem exatamente um elemento raiz. Todos os elementos do esquema de perfil de banda larga móvel usados pelo Windows 7 estão no namespace `https://www.microsoft.com/networking/WWAN/profile/v1` e os elementos usados pelo Windows 8 estão no namespace `https://www.microsoft.com/networking/WWAN/profile/v2` .

O esquema de perfil de banda larga móvel impõe estritamente a ordem dos nós. Os nós especificados em um perfil devem aderir ao **esquema de perfil de banda larga móvel** e aparecer na ordem prescrita na definição do esquema. Por exemplo, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) deve ser especificado imediatamente após [**accessstring**](schema-accessstring-contexttype-element.md).

-   [Esquema de perfil de banda larga móvel v1](mobile-broadband-profile-schema.md)
-   [Esquema de perfil de banda larga móvel v2](mobile-broadband-profile-schema-v2.md)
-   [Esquema de perfil de banda larga móvel v3](mobile-broadband-profile-schema-v3.md)
-   [Esquema de perfil de banda larga móvel v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 
