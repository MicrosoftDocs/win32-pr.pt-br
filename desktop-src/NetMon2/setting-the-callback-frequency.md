---
description: Use o código a seguir para definir a frequência de retorno de chamada.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Definindo a frequência de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296422"
---
# <a name="setting-the-callback-frequency"></a>Definindo a frequência de retorno de chamada

Use o código a seguir para definir a frequência de retorno de chamada:

**Valor DWORD** Valor = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Este fragmento de código define a frequência de retorno de chamada como 1 segundo (o valor mínimo). O valor máximo deve ser muito maior que 1. Se o buffer do NPP (provedor de pacotes de rede) estiver cheio, o NPP chamará o monitor novamente mais cedo.

 

 



