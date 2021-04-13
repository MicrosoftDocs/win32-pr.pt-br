---
description: Um perfil de política de WLAN (rede local sem fio) nativo do wifi é composto pelos seguintes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Elementos do esquema de WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501559"
---
# <a name="wlan_policy-schema-elements"></a>Elementos do esquema de política de WLAN \_

Um perfil de política de WLAN (rede local sem fio) nativo do wifi é composto pelos seguintes elementos de esquema. Todos os elementos nomeados estão no namespace `https://www.microsoft.com/networking/WLAN/policy/v1` .

A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil. A ordem dos elementos é imposta. Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.

Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil, pois elementos podem ser adicionados em **xs: qualquer** ponto de inserção.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**nome (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Descrição (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**permitirlist (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**rede (permitirlist)**](wlan-policyschema-network-allowlist-element.md)
                -   [**NetworkName (networkitemtype)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**NetworkType (networkitemtype)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**Blocklist (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**rede (bloquearlist)**](wlan-policyschema-network-blocklist-element.md)
                -   [**NetworkName (networkitemtype)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**NetworkType (networkitemtype)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**ProfileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



