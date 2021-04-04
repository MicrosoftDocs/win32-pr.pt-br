---
description: Todos os objetos protegíveis organizam seus direitos de acesso usando o formato de máscara de acesso mostrado na ilustração a seguir.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato de máscara de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828832"
---
# <a name="access-mask-format"></a>Formato de máscara de acesso

Todos os objetos protegíveis organizam seus direitos de acesso usando o formato de [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) mostrado na ilustração a seguir.

![formato de máscara de acesso](images/accctrl4.png)

Nesse formato, os 16 bits de ordem inferior são para direitos de acesso específicos de objeto, os próximos 8 bits são para [direitos de acesso padrão](standard-access-rights.md), que se aplicam à maioria dos tipos de objetos e os quatro bits de ordem superior são usados para especificar [direitos de acesso genéricos](generic-access-rights.md) que cada tipo de objeto pode mapear para um conjunto de direitos padrão e específicos de objeto. O bit de segurança do sistema de acesso \_ \_ corresponde ao [direito de acessar a SACL do objeto](sacl-access-right.md).

 

 
