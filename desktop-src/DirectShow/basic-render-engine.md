---
description: Mecanismo de renderização básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Mecanismo de renderização básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955565"
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

[Renderizando um Project](rendering-a-project.md)
</dt> <dt>

[Mecanismo de processamento inteligente](smart-render-engine.md)
</dt> </dl>

 

 



