---
description: Esquema de perfil de banda larga móvel v3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Esquema de perfil de banda larga móvel v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3fb4e939da9cbedadf8549539f73d0776e1636c6a0aea64a2cee2e7134e3edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881569"
---
# <a name="mobile-broadband-profile-schema-v3"></a>Esquema de perfil de banda larga móvel v3

O Windows 8Pacote de Perfil de Banda Larga Móvel v3 está disponível no namespace `https://www.microsoft.com/networking/WWAN/profile/v3` .

-   [Elementos do esquema de perfil de banda larga móvel v3](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



