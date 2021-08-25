---
description: Manipulando alterações de formato do renderador de vídeo
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Manipulando alterações de formato do renderador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1dd0ec2f87a8604d3b03aa6c2f334161d218f4d7fb45c76aad1015f071d947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905296"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Manipulando alterações de formato do renderador de vídeo

Esta seção descreve como um filtro de decodificador ou filtro de transformação deve manipular alterações de formato do renderização de vídeo.

**Filtro do renderador de vídeo**

Quando o filtro [antigo do Video Renderer](video-renderer-filter.md) se conecta, ele requer um formato RGB que corresponde ao formato de exibição do monitor primário. Isso permite que ele use o GDI para renderização se o DirectDraw não estiver disponível. Quando a reprodução é iniciada, o Renderador de Vídeo pode mudar para um formato compatível com DirectDraw. Para verificar se o filtro upstream pode dar suporte ao novo formato, o Renderador de Vídeo chama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída do filtro upstream. Se o filtro upstream aceitar o novo formato, o **método QueryAccept** retornará S \_ OK. O Renderador de Vídeo alterna formatos anexando um tipo de mídia com o novo formato ao próximo exemplo de mídia retornado por seu alocador. O filtro upstream deve verificar se há alterações de formato chamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) em cada exemplo. O Renderador de Vídeo pode alternar entre o formato original e o novo formato a qualquer momento durante o streaming. Ele não chama **QueryAccept após** a primeira alteração de formato. Depois que o filtro upstream aceitar o novo formato, ele deverá ser capaz de alternar para frente e para trás.

O filtro upstream pode rejeitar a alteração de formato retornando S \_ FALSE de **QueryAccept**. Nesse caso, o Renderador de Vídeo continua a usar o GDI com o formato original.

**Filtro de renderização de combinação de vídeo**

O filtro de Renderização de Combinação de Vídeo (VMR-7 e VMR-9) se conectará a qualquer formato que seja suportado pelo hardware de gráficos no sistema. A VMR-7 sempre usa DirectDraw para renderização e aloca as superfícies subjacentes do DirectDraw quando o filtro upstream se conecta. A VMR-9 sempre usa o Direct3D para renderização e aloca as superfícies direct3D subjacentes quando o filtro upstream se conecta.

O hardware gráfico pode exigir uma distância de superfície maior do que a largura da imagem. Nesse caso, a VMR solicita um novo formato chamando **QueryAccept.** Ele relata o avanço da superfície **no membro biWidth** do [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no formato de vídeo. Se o filtro upstream não retornar S OK de \_ **QueryAccept,** a VMR rejeitará o formato e tentará se conectar usando o próximo formato anunciado pelo filtro upstream. A VMR anexa o tipo de mídia com o novo formato ao primeiro exemplo de mídia. Após o primeiro exemplo, o formato permanece constante; A VMR não alterna formatos enquanto o grafo está em execução.

**EVR (Renderização de Vídeo Aprimorada)**

O EVR sempre usa Direct3D para renderização. Se um avanço de superfície maior for necessário, o EVR usará o mesmo mecanismo **QueryAccept** que a VMR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[QueryAccept (Upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



