---
description: O DC de informações é usado para recuperar dados de dispositivo padrão.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contextos do dispositivo de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779126"
---
# <a name="information-device-contexts"></a>Contextos do dispositivo de informações

O DC de informações é usado para recuperar dados de dispositivo padrão. Por exemplo, um aplicativo pode chamar a função [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) para criar um DC de informações para um modelo específico de impressora e, em seguida, chamar as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) para recuperar os atributos padrão de caneta ou pincel. Como o sistema pode recuperar informações do dispositivo sem criar as estruturas normalmente associadas aos outros tipos de contextos de dispositivo, um DC de informações envolve muito menos sobrecarga e é criado significativamente mais rapidamente do que qualquer um dos outros tipos. Depois que um aplicativo concluir a recuperação de dados usando um DC de informações, ele deverá chamar a [**função DeleteDC.**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)

 

 



