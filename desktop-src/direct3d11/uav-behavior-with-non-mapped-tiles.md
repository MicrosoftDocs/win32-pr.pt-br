---
title: Comportamento de UAV com blocos não mapeados
description: O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916025"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportamento de UAV com blocos não mapeados

O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware. Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos. Esta seção resume o comportamento ideal.

As operações de sombreador que lêem a partir de um bloco não mapeado em um UAV retornam 0 em todos os componentes sem perder o formato e o padrão para componentes que estão faltando.

As operações de sombreador que tentam gravar em um bloco não mapeado fazem com que nada seja gravado na área não mapeado (enquanto as gravações em uma área mapeada prosseguem). Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




