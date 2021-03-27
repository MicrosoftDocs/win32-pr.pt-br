---
title: Comportamento de rasterizador com blocos não mapeados
description: Esta seção descreve o comportamento de rasterizador com blocos não mapeados.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988516"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Comportamento de rasterizador com blocos não mapeados

Esta seção descreve o comportamento de rasterizador com blocos não mapeados.

## <a name="depthstencilview"></a>DepthStencilView

O comportamento de leituras e gravações do modo de exibição de estêncil de profundidade (DSV) depende do nível de suporte de hardware. Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos.

Aqui está o comportamento ideal:

Se um bloco não estiver mapeado no DepthStencilView, o valor de retorno de profundidade de leitura será 0, o que será enviado, em seguida, para todas as operações configuradas para o valor de leitura de profundidade. Gravações para blocos de profundidade ausentes serão ignoradas. Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.

## <a name="rendertargetview"></a>RenderTargetView

O comportamento leituras e gravações de modo de exibição de destino de renderização (RTV) depende do nível de suporte de hardware. Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos.

Em todas as implementações, diferentes RTVs (e DSV) associados ao mesmo tempo podem ter diferentes áreas mapeadas versus não mapeadas e podem ter diferentes formatos de superfície dimensionados (o que significa formas de bloco diferentes).

Aqui está o comportamento ideal:

Leituras de RTVs retornam 0 em blocos ausentes e gravações são ignoradas. Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




