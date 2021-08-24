---
description: Use o código a seguir para definir a frequência de retorno de chamada.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Definindo a frequência de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363242"
---
# <a name="setting-the-callback-frequency"></a>Definindo a frequência de retorno de chamada

Use o código a seguir para definir a frequência de retorno de chamada:

**Valor DWORD** Valor = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Este fragmento de código define a frequência de retorno de chamada como 1 segundo (o valor mínimo). O valor máximo deve ser muito maior que 1. Se o buffer do NPP (provedor de pacotes de rede) estiver cheio, o NPP chamará o monitor novamente mais cedo.

 

 



