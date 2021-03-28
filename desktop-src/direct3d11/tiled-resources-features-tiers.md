---
title: Recursos de azulejos recursos camadas
description: O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de camada de recursos lado-a-D3D11 \_ \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916026"
---
# <a name="tiled-resources-features-tiers"></a>Recursos de azulejos recursos camadas

O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de [**\_ \_ \_ camada de recursos lado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) -a-D3D11.

Para consultar se o hardware e o driver dão suporte a recursos de lado e em qual nível de camada, passe o valor de [**D3D11 do \_ recurso \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) para o parâmetro *Feature* de [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Além disso, passe um ponteiro para a estrutura [**D3D11 de \_ dados do recurso \_ \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) para o parâmetro *pFeatureSupportData* e passe o tamanho da estrutura D3D11 D3D11 de **\_ \_ dados de \_ \_ recursos** OPTIONS1 para o parâmetro *FeatureSupportDataSize* . **CheckFeatureSupport** retorna o nível de camada como um valor de [**camada de recursos com lado de D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) no membro **TiledResourcesTier** de **D3D11 de dados de \_ recursos \_ \_ D3D11 \_ OPTIONS1**.

Esta seção descreve essas duas camadas.

## <a name="in-this-section"></a>Nesta seção



| Tópico                           | Descrição                                       |
|---------------------------------|---------------------------------------------------|
| [Camada 1](tier-1.md)<br/> | Esta seção descreve o suporte de nível 1.<br/> |
| [Camada 2](tier-2.md)<br/> | Esta seção descreve o suporte de camada 2.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos em ladrilho](tiled-resources.md)
</dt> </dl>

 

 





