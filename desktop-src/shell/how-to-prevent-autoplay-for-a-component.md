---
description: Ilustra qual chave do registro deve ser definida para evitar a reprodução automática.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Como evitar a reprodução automática para um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967895"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Como evitar a reprodução automática para um componente

Ilustra qual chave do registro deve ser definida para evitar a reprodução automática.

## <a name="instructions"></a>Instruções


Para evitar que a reprodução automática seja iniciada em resposta a um evento, adicione o seguinte valor de **reg \_ sz** , conforme mostrado neste exemplo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

O valor é o identificador de classe (CLSID) que o componente que está gerando o evento é conhecido pelo na corrompidos (tabela de objetos em execução). O valor não tem dados.

> [!IMPORTANT]
> Sob essa chave, os CLSIDs não são colocados entre chaves ( {} ).

 

 

 



