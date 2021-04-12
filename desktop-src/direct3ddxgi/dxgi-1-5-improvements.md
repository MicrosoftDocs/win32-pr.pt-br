---
description: A funcionalidade a seguir foi adicionada à infraestrutura de gráficos do Microsoft DirectX (DXGI) 1,5 para dar suporte à especificação e à duplicação de formatos de saída mais flexíveis.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Aprimoramentos de DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298034"
---
# <a name="dxgi-15-improvements"></a>Aprimoramentos de DXGI 1,5

A funcionalidade a seguir foi adicionada à infraestrutura de gráficos do Microsoft DirectX (DXGI) 1,5 para dar suporte à especificação e à duplicação de formatos de saída mais flexíveis.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Ampla gama de cores e intervalos dinâmicos

Consulte [usando o DirectX com altas exibições de intervalo dinâmico e cor avançada](../direct3darticles/high-dynamic-range.md).

## <a name="variable-refresh-rate-displays"></a>Exibição da taxa de atualização da variável

Consulte a [taxa de atualização de variável exibida](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicando saída

Uma única interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), com um único método, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), foi adicionada ao dxgi 1,5 para fornecer uma versão de desempenho mais flexível e mais alta do método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original. **DuplicateOutput1** permite especificar uma lista de formatos com suporte para superfícies de tela inteira que podem ser retornadas pelo objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e habilita a captura de conteúdo HDR e WCG.

## <a name="offering-and-reclaiming-resources"></a>Oferta e recuperação de recursos

Os métodos atualizados [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) foram adicionados a uma nova interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), para permitir a desconfirmação da memória, além de descartar recursos. A permissão para o novo [**sinalizador de recurso de oferta de dxgi permite o sinalizador de \_ \_ \_ \_ \_ desconfirmação**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) significa que os novos resultados de recuperações devem ser tratados adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
