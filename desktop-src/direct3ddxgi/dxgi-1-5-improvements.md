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
# <a name="dxgi-15-improvements"></a><span data-ttu-id="f1d04-103">Aprimoramentos de DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="f1d04-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="f1d04-104">A funcionalidade a seguir foi adicionada à infraestrutura de gráficos do Microsoft DirectX (DXGI) 1,5 para dar suporte à especificação e à duplicação de formatos de saída mais flexíveis.</span><span class="sxs-lookup"><span data-stu-id="f1d04-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="f1d04-105">Ampla gama de cores e intervalos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="f1d04-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="f1d04-106">Consulte [usando o DirectX com altas exibições de intervalo dinâmico e cor avançada](../direct3darticles/high-dynamic-range.md).</span><span class="sxs-lookup"><span data-stu-id="f1d04-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="f1d04-107">Exibição da taxa de atualização da variável</span><span class="sxs-lookup"><span data-stu-id="f1d04-107">Variable refresh rate displays</span></span>

<span data-ttu-id="f1d04-108">Consulte a [taxa de atualização de variável exibida](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="f1d04-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="f1d04-109">Duplicando saída</span><span class="sxs-lookup"><span data-stu-id="f1d04-109">Duplicating output</span></span>

<span data-ttu-id="f1d04-110">Uma única interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), com um único método, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), foi adicionada ao dxgi 1,5 para fornecer uma versão de desempenho mais flexível e mais alta do método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original.</span><span class="sxs-lookup"><span data-stu-id="f1d04-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="f1d04-111">**DuplicateOutput1** permite especificar uma lista de formatos com suporte para superfícies de tela inteira que podem ser retornadas pelo objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e habilita a captura de conteúdo HDR e WCG.</span><span class="sxs-lookup"><span data-stu-id="f1d04-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="f1d04-112">Oferta e recuperação de recursos</span><span class="sxs-lookup"><span data-stu-id="f1d04-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="f1d04-113">Os métodos atualizados [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) foram adicionados a uma nova interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), para permitir a desconfirmação da memória, além de descartar recursos.</span><span class="sxs-lookup"><span data-stu-id="f1d04-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="f1d04-114">A permissão para o novo [**sinalizador de recurso de oferta de dxgi permite o sinalizador de \_ \_ \_ \_ \_ desconfirmação**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) significa que os novos resultados de recuperações devem ser tratados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="f1d04-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d04-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1d04-115">Related topics</span></span>

[<span data-ttu-id="f1d04-116">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="f1d04-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
