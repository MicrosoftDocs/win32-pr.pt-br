---
description: Um perfil de política WLAN (Lan sem fio Wi-Fi) nativo é composto pelos seguintes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92bfca66e1eff2c8c180968c83b5dbb565d1d4aa27ace1ba89d1c70634d6e7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619541"
---
# <a name="wlan_policy-schema-elements"></a>Elementos de \_ esquema de política WLAN

Um perfil de política WLAN (Lan sem fio Wi-Fi) nativo é composto pelos seguintes elementos de esquema. Todos os elementos nomeados estão no namespace `https://www.microsoft.com/networking/WLAN/policy/v1` .

A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil. A ordenação de elementos é imposta. Nem todos os elementos estão em cada perfil, pois alguns elementos são opcionais.

Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil, pois os elementos podem ser **adicionados em xs:any pontos** de inserção.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**name (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**description (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**allowList (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**blockList (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



