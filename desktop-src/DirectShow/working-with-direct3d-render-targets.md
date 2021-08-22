---
description: Trabalhando com destinos de renderização direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Trabalhando com destinos de renderização direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7bacf36402b071d60989e225cdcd9533500494a0593bcf9753ddc06bb93ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650336"
---
# <a name="working-with-direct3d-render-targets"></a>Trabalhando com destinos de renderização direct3D

Vários subtipos de mídia para destinos de renderização direct3D são definidos para uso com a VMR-7 e a VMR-9. Quando um filtro upstream propõe uma conexão com um desses subtipos, ele indica à VMR que a renderização deve ser executada em um destino de renderização Direct3D. Para a VMR-7, esse será um destino de renderização DirectX 7 Direct3D e, para a VMR-9, esse será um destino de renderização DirectX 9 Direct3D. Se a VMR estiver no modo de combinação, a superfície também será uma superfície de textura Direct3D. Se a VMR não estiver no modo de combinação, a superfície será uma superfície Direct3D normal. Os formatos de pixel ARGB só têm suporte quando a VMR está no modo de combinação. Os subtipos de destino de renderização são:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Esses tipos são definidos no arquivo de header uuids.h. Os tipos de mídia MEDIASUBTYPE RGB32 são um formato RGBx888 e os tipos de mídia \_ MEDIASUBTYPE RGB16 são um \_ formato RGB565. Para obter mais informações sobre esses formatos de pixel, consulte a documentação do DirectX Graphics.

**Solicitando uma superfície desbloqueada**

O bloqueio e o desbloqueio de superfícies do DirectDraw são operações computacionalmente caras. Ao usar os subtipos de mídia de destino de renderização direct3D, o filtro upstream precisa que as superfícies sejam desbloqueadas para que ele possa operar neles com o hardware gráfico. Para evitar uma operação desnecessária de desbloqueio de bloqueio, a VMR dá suporte a um novo sinalizador no método [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) AM \_ GBF NODDSURFACELOCK, que instrui a VMR a não bloquear a superfície do DirectDraw antes de passar um exemplo para o \_ filtro upstream. Quando esse sinalizador é usado, as chamadas para [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) falharão porque não há ponteiro bloqueado. Para obter acesso à superfície do DirectDraw, o filtro deve chamar **QueryInterface** no objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) retornado e solicitar a interface [**IVMRSurface.**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) Obviamente, o filtro upstream deve garantir que a superfície não seja bloqueada quando liberar o exemplo de volta para a lista gratuita.

 

 



