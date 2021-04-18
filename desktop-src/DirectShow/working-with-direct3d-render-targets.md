---
description: Trabalhando com destinos de renderização do Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Trabalhando com destinos de renderização do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783315"
---
# <a name="working-with-direct3d-render-targets"></a>Trabalhando com destinos de renderização do Direct3D

Vários subtipos de mídia para destinos de renderização do Direct3D são definidos para uso com o VMR-7 e o VMR-9. Quando um filtro upstream propõe uma conexão com um desses subtipos, ele indica ao VMR que a renderização deve ser executada em um destino de renderização do Direct3D. Para o VMR-7, esse será um destino de renderização do Direct3D do DirectX 7 e para o VMR-9, este será um destino de renderização do Direct3D do DirectX 9. Se o VMR estiver no modo de mistura, a superfície também será uma superfície de textura de Direct3D. Se o VMR não estiver no modo de mistura, a superfície será uma superfície do Direct3D normal. Os formatos de pixel ARGB só têm suporte quando o VMR está no modo de mistura. Os subtipos de destino de renderização são:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Esses tipos são definidos no arquivo de cabeçalho UUIDs. h. Os \_ tipos de mídia MEDIASUBTYPE RGB32 são um formato RGBx888 e os \_ tipos de mídia MEDIASUBTYPE RGB16 são um formato RGB565. Para obter mais informações sobre esses formatos de pixel, consulte a documentação de gráficos do DirectX.

**Solicitando uma superfície desbloqueada**

O bloqueio e o desbloqueio das superfícies do DirectDraw são operações de custo computacional. Ao usar os subtipos de mídia de destino do Direct3D render, o filtro upstream precisa que as superfícies sejam desbloqueadas para que possam operar com o hardware de gráficos. Para evitar uma operação desbloqueada de bloqueio desnecessário, o VMR dá suporte a um novo sinalizador no método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , \_ gbf \_ NODDSURFACELOCK, que instrui o VMR a não bloquear a superfície do DirectDraw antes de passar um exemplo para o filtro upstream. Quando esse sinalizador é usado, as chamadas para [**IMediaSample:: Getpointr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) falharão porque não há nenhum ponteiro bloqueado. Para obter acesso à superfície do DirectDraw, o filtro deve chamar **QueryInterface** no objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) retornado e solicitar a interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Obviamente, o filtro upstream deve garantir que a superfície não esteja bloqueada quando libera o exemplo de volta para a lista gratuita.

 

 



