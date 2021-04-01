---
description: Detector de mídia (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de mídia (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091883"
---
# <a name="media-detector-mediadet"></a>Detector de mídia (MediaDet)

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto detector de mídia (MediaDet) recupera informações de formato e ainda quadros de fontes de arquivo. O detector de mídia não exige que o Gerenciador de gráficos de filtro funcione. Para criar esse objeto, chame **CoCreateInstance**. O identificador de classe é CLSID \_ MediaDet.

Para ler arquivos do Windows Media™, o aplicativo deve fornecer um certificado de software, também chamado de chave. Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** do detector de mídia. Para obter mais informações, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).

O objeto MediaDet expõe as seguintes interfaces:

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



