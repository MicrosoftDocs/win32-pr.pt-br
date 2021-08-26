---
description: A linha do tempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: A linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049996"
---
# <a name="the-timeline"></a>A linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

A linha do tempo expõe a interface [**IAMTimeline.**](iamtimeline.md) Essa interface contém métodos para definir propriedades na linha do tempo; para adicionar grupos à linha do tempo; e para criar objetos de linha do tempo, como grupos, faixas e fontes. Para criar uma nova linha do tempo, chame a **função CoCreateInstance** padrão da seguinte forma:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



A nova linha do tempo está vazia. Neste ponto, você pode carregar um arquivo de projeto existente (consulte Carregando e visualizando um Project ) ou criar [a](loading-and-previewing-a-project.md)linha do tempo criando e inserindo novos objetos (consulte Construindo uma linha do [tempo).](constructing-a-timeline.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



