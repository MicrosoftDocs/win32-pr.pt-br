---
title: Comportamento de SRV com blocos não mapeados
description: O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159282"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>Comportamento de SRV com blocos não mapeados

O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware. Para obter uma análise dos requisitos, confira comportamento de leitura para [camadas de recursos de recursos de lado](tiled-resources-features-tiers.md). Esta seção resume o comportamento ideal, que o [Nível 2](tier-2.md) requer.

Considere uma operação de filtro de textura que lê de um conjunto de texels em um SRV. Texels que se enquadram em blocos não mapeados contribuem com 0 em todos os componentes sem perder o formato (e o padrão para componentes que estão faltando) para a operação de filtro geral junto com contribuições de texels mapeadas. Os texels são todos ponderados e combinados juntos independentemente dos dados serem provenientes de blocos mapeados ou não mapeados.

Alguns hardwares de nível de [camada 2](tier-2.md) de primeira geração não atendem a esse requisito de especificação e retorna o 0 com os padrões descritos anteriormente como o resultado de filtro geral se qualquer texels (com peso diferente de zero) cair em blocos não mapeados. O requisito de incluir todos os texels no filtro (peso diferente de zero) não poderá faltar em nenhum outro hardware.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




