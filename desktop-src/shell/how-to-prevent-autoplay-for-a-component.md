---
description: Ilustra qual chave do Registro deve ser definida para evitar a Reprodução Automática.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Como evitar a reprodução automática para um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859683"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Como evitar a reprodução automática para um componente

Ilustra qual chave do Registro deve ser definida para evitar a Reprodução Automática.

## <a name="instructions"></a>Instruções


Para impedir que o AutoPlay seja lançado em resposta a um evento, adicione o seguinte **valor REG \_ SZ,** conforme mostrado neste exemplo.

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

O valor é o CLSID (identificador de classe) que o componente que está gerando o evento é conhecido por na ROT (tabela de objetos em execução). O valor não tem dados.

> [!IMPORTANT]
> Sob essa chave, as CLSIDs não são entre chaves ( {} ).

 

 

 



