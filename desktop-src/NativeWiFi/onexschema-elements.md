---
description: Um perfil 802.1 X contém os seguintes elementos de esquema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementos de esquema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662141"
---
# <a name="onex-schema-elements"></a>Elementos de esquema OneX

Um perfil 802.1 X contém os seguintes elementos de esquema. Todos os elementos de esquema de OneX se aplicam a perfis com e sem fio. A maioria dos elementos nomeados está no namespace `https://www.microsoft.com/networking/OneX/v1` , com exceção de [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) , que está no namespace `https://www.microsoft.com/provisioning/EapHostConfig` .

A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil. A ordem dos elementos é imposta. Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.

Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil, pois elementos podem ser adicionados em **xs: qualquer** ponto de inserção.

-   [**802.1x**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**suplicante (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**AuthMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**Logon único (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**tipo (logon único)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (logon único)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (logon único)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



