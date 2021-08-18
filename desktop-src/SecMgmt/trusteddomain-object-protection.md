---
description: Quando um objeto TrustedDomain é criado, ele recebe uma proteção padrão.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Proteção de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e34eac9b9e3a021db7580803cec6c99f6489d01c9499b28251cb262b721fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004794"
---
# <a name="trusteddomain-object-protection"></a>Proteção de objeto TrustedDomain

Quando um [**objeto TrustedDomain**](trusteddomain-object.md) é criado, ele recebe uma proteção padrão da seguinte forma:

-   O grupo local WORLD tem acesso GENERIC \_ EXECUTE.
-   O grupo local \_ ADMINISTRADOR LOCAL tem acesso DELETE, GENERIC \_ READ, GENERIC WRITE e GENERIC \_ \_ EXECUTE.
-   O grupo \_ local ADMINISTRADOR LOCAL é atribuído como proprietário e grupo primário do objeto .

 

 



