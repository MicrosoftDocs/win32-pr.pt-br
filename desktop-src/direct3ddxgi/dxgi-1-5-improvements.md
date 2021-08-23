---
description: A funcionalidade a seguir foi adicionada ao Microsoft DirectX Graphic Infrastructure (DXGI) 1.5, para dar suporte à especificação e à duplicação mais flexíveis de formatos de saída.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Melhorias do DXGI 1.5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 52661018941f84a14f45c112ba7ed68800d0cf0f2fb69f7a1d3333651fb17787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987126"
---
# <a name="dxgi-15-improvements"></a>Melhorias do DXGI 1.5

A funcionalidade a seguir foi adicionada ao Microsoft DirectX Graphic Infrastructure (DXGI) 1.5, para dar suporte à especificação e à duplicação mais flexíveis de formatos de saída.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Alto Alcance Dinâmico e wide color gamut

Consulte [Usando o DirectX com exibições de alto intervalo dinâmico e cor avançada.](../direct3darticles/high-dynamic-range.md)

## <a name="variable-refresh-rate-displays"></a>A taxa de atualização variável é exibida

Consulte Taxa [de atualização variável exibe](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicando a saída

Uma única interface, [**IDXGIOutput5,**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)com um único método, [**DuplicateOutput1,**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)foi adicionada ao DXGI 1.5 para fornecer uma versão de desempenho mais flexível e superior do método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original. **DuplicateOutput1** permite especificar uma lista de formatos com suporte para superfícies de tela inteira que podem ser retornados pelo objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e permite capturar o conteúdo de HDR e WCG.

## <a name="offering-and-reclaiming-resources"></a>Oferecendo e recuperando recursos

Os métodos [**Atualizados OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) foram adicionados a uma nova interface, [**IDXGIDevice4,**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)para permitir a desassoçamento de memória, além de descartar recursos. Optar pelo novo sinalizador [**DXGI \_ OFFER RESOURCE FLAG ALLOW \_ \_ \_ \_ DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) significa que os novos resultados da recuperação devem ser tratados corretamente.

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
