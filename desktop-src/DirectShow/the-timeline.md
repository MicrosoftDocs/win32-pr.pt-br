---
description: A linha do tempo
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: A linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760870"
---
# <a name="the-timeline"></a>A linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

A linha do tempo expõe a interface [**IAMTimeline**](iamtimeline.md) . Esta interface contém métodos para definir propriedades na linha do tempo; para adicionar grupos à linha do tempo; e para criar objetos de linha do tempo, como grupos, faixas e fontes. Para criar uma nova linha do tempo, chame a função **CoCreateInstance** padrão da seguinte maneira:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



A nova linha do tempo está vazia. Neste ponto, você pode carregar um arquivo de projeto existente (consulte [carregando e visualizando um projeto](loading-and-previewing-a-project.md)), ou criar a linha do tempo criando e inserindo novos objetos (consulte [construindo uma linha do tempo](constructing-a-timeline.md)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



