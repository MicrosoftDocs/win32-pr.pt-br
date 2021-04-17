---
description: 'Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anunciando um aplicativo Per-User para ser instalado com privilégios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768488"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Anunciando um aplicativo Per-User para ser instalado com privilégios elevados

Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:

-   Seu processo deve ser um serviço executado na conta do sistema LocalSystem no Windows XP ou posterior.
-   Gere um script de anúncio chamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) ou [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).
-   Seu processo deve representar o usuário que é o destino do anúncio.
-   Chame [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e use os sinalizadores SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| \_ \_ \| \_ SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.

Ao seguir as diretrizes, você anuncia um aplicativo para um usuário especificado e, quando o usuário opta por instalar, o aplicativo é instalado com privilégios elevados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação de patch em aplicativos gerenciados por usuário](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



