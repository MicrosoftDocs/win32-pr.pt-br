---
description: Mecanismo de processamento inteligente
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Mecanismo de processamento inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779836"
---
# <a name="smart-render-engine"></a>Mecanismo de processamento inteligente

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto do mecanismo de processamento inteligente renderiza a saída compactada de uma linha do tempo. Para criar esse objeto, chame **CoCreateInstance**. Para saída não compactada, use o mecanismo de renderização básico. O identificador de classe é CLSID \_ SmartRenderEngine.

O mecanismo de processamento inteligente expõe as seguintes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um projeto](rendering-a-project.md)
</dt> <dt>

[Mecanismo de renderização básico](basic-render-engine.md)
</dt> </dl>

 

 



