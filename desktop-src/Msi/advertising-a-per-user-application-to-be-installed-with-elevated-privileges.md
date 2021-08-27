---
description: 'Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anunciando um aplicativo Per-User para ser instalado com privilégios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdced246f90a345b5b2cc599541119a26e29e4d9a1d708be1ee8299d55d3c28d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082956"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Anunciando um aplicativo Per-User para ser instalado com privilégios elevados

Para anunciar um aplicativo em uma base de instalação por usuário quando o aplicativo requer privilégios elevados (ou seja, do sistema) para instalação, use as diretrizes na lista a seguir:

-   seu processo deve ser um serviço executado na conta do sistema LocalSystem no Windows XP ou posterior.
-   Gere um script de anúncio chamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) ou [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).
-   Seu processo deve representar o usuário que é o destino do anúncio.
-   Chame [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e use os sinalizadores SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| \_ \_ \| \_ SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.

Ao seguir as diretrizes, você anuncia um aplicativo para um usuário especificado e, quando o usuário opta por instalar, o aplicativo é instalado com privilégios elevados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação de patch em aplicativos gerenciados por usuário](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



