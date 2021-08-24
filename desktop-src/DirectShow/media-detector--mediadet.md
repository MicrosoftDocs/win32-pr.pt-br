---
description: Detector de Mídia (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de Mídia (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684966"
---
# <a name="media-detector-mediadet"></a>Detector de Mídia (MediaDet)

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto MediaDet (MediaDet) recupera informações de formato e ainda quadros de fontes de arquivo. O Detector de Mídia não exige que o Gerenciador Graph Filtro funcione. Para criar esse objeto, chame **CoCreateInstance**. O identificador de classe é CLSID \_ MediaDet.

Para ler Windows mídia™, o aplicativo deve fornecer um certificado de software, também chamado de chave. Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** do Detector de Mídia. Para obter mais informações, consulte [Desbloqueando o SDK Windows Formato de Mídia.](unlocking-the-windows-media-format-sdk.md)

O objeto MediaDet expõe as seguintes interfaces:

-   [**IMediaDet**](imediadet.md)
-   **Iobjectwithsite**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



