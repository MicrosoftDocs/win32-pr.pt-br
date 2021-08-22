---
description: Todos os objetoscuráveis organizam seus direitos de acesso usando o formato de máscara de acesso mostrado na ilustração a seguir.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato de máscara de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86187f5ef69eb115bc880d2bc4df07e8b1a1f791976da2a8d24b6a0f9d7293c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914522"
---
# <a name="access-mask-format"></a>Formato de máscara de acesso

Todos os objetoscuráveis organizam seus direitos de acesso usando o [*formato de máscara de*](/windows/desktop/SecGloss/a-gly) acesso mostrado na ilustração a seguir.

![formato de máscara de acesso](images/accctrl4.png)

Nesse formato, os 16 bits de ordem baixa são para direitos de acesso específicos ao objeto, os próximos 8 bits são para [](generic-access-rights.md) direitos de acesso padrão [,](standard-access-rights.md)que se aplicam à maioria dos tipos de objetos e os quatro bits de ordem alta são usados para especificar direitos de acesso genéricos que cada tipo de objeto pode mapear para um conjunto de direitos padrão e específicos do objeto. O bit \_ ACCESS SYSTEM SECURITY corresponde à direita para acessar a \_ [SACL do objeto.](sacl-access-right.md)

 

 
