---
description: Mecanismo de renderização básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Mecanismo de renderização básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500592"
---
# <a name="basic-render-engine"></a>Mecanismo de renderização básico

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto do mecanismo de renderização básico renderiza a saída não compactada de uma linha do tempo. Para criar esse objeto, chame **CoCreateInstance**. Para saída compactada, use o mecanismo de processamento inteligente. O identificador de classe é CLSID \_ RenderEngine.

O mecanismo de renderização básico expõe as seguintes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um projeto](rendering-a-project.md)
</dt> <dt>

[Mecanismo de processamento inteligente](smart-render-engine.md)
</dt> </dl>

 

 



