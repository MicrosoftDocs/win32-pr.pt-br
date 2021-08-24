---
title: Obtendo os recursos de um driver de captura
description: Obtendo os recursos de um driver de captura
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS mensagem
- macro capDriverGetCaps
- Estrutura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6f717f1a7c19878ceeca2cccc2db309be3e62e0febf90dcb23376db73eed17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806566"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a>Obtendo os recursos de um driver de captura

A [**mensagem \_ \_ \_ obter \_ Caps do driver do WM Cap**](wm-cap-driver-get-caps.md) retorna os recursos do driver de captura e o hardware subjacente na estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) . Cada vez que um aplicativo conecta um novo driver de captura à janela de captura, ele deve atualizar a estrutura **CAPDRIVERCAPS** . O exemplo a seguir usa a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para obter os recursos do driver de captura.


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




