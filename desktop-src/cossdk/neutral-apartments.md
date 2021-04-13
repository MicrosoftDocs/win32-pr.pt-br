---
description: O COM+ apresenta Apartments neutro para simplificar a programação em ambientes multi-threaded. O apartamento neutro é o modelo preferencial para COM+ para componentes sem interface do usuário.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Apartments neutro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370425"
---
# <a name="neutral-apartments"></a>Apartments neutro

O COM+ apresenta Apartments neutro para simplificar a programação em ambientes multi-threaded. O apartamento neutro é o modelo preferencial para COM+ para componentes sem interface do usuário.

No passado, para evitar gargalos, os desenvolvedores de COM+ que precisam de escalabilidade de servidor precisavam implementar componentes de thread livre; no entanto, os modelos de Threading livre são complicados de implementar, pois eles devem lidar com o acesso de interbloqueio. Em apartments neutros, os objetos seguem as diretrizes para Apartments multithread, mas podem ser executados em qualquer tipo de thread. Quando um thread está sendo executado em um apartamento neutro, o contexto do objeto é recebido sem causar uma alternância de thread.

Cada processo pode ter apenas um apartamento neutro. Para selecionar um apartamento neutro, use a seguinte configuração do registro:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

Os componentes que têm interfaces de usuário devem continuar usando Apartments de thread único como o modelo preferencial. Para selecionar um apartamento de thread único, use a seguinte configuração de registro:

**ThreadingModel** = apartamento

 

 



