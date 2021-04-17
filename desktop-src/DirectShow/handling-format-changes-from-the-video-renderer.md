---
description: Manipulando alterações de formato do processador de vídeo
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Manipulando alterações de formato do processador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748000"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Manipulando alterações de formato do processador de vídeo

Esta seção descreve como um filtro de decodificador ou de transformação deve tratar as alterações de formato do processador de vídeo.

**Filtro de renderização de vídeo**

Quando o filtro antigo do [processador de vídeo](video-renderer-filter.md) se conecta, ele requer um formato RGB que corresponda ao formato de exibição do monitor primário. Isso permite que ele use GDI para renderização se o DirectDraw não estiver disponível. Quando a reprodução é iniciada, o processador de vídeo pode mudar para um formato compatível com o DirectDraw. Para verfify se o filtro upstream pode dar suporte ao novo formato, o processador de vídeo chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída do filtro upstream. Se o filtro upstream aceitar o novo formato, o método **QueryAccept** retornará S \_ OK. O processador de vídeo alterna os formatos anexando um tipo de mídia com o novo formato à próxima amostra de mídia retornada por seu alocador. O filtro upstream deve verificar se há alterações de formato chamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) em cada exemplo. O processador de vídeo pode alternar entre o formato original e o novo formato a qualquer momento durante o streaming. Ele não chama **QueryAccept** após a primeira alteração de formato. Depois que o filtro upstream aceitar o novo formato, ele deverá ser capaz de alternar para frente e para trás.

O filtro upstream pode rejeitar a alteração de formato retornando S \_ false de **QueryAccept**. Nesse caso, o processador de vídeo continua a usar o GDI com o formato original.

**Filtro de processador de mixagem de vídeo**

O filtro de processador de mixagem de vídeo (VMR-7 e VMR-9) se conectará com qualquer formato que tenha suporte do hardware de gráficos no sistema. O VMR-7 sempre usa o DirectDraw para renderização e aloca as superfícies do DirectDraw subjacentes quando o filtro upstream se conecta. O VMR-9 sempre usa o Direct3D para renderização e aloca as superfícies do Direct3D subjacentes quando o filtro upstream se conecta.

O hardware de gráficos pode exigir um stride de superfície maior do que a largura da imagem. Nesse caso, o VMR solicita um novo formato chamando **QueryAccept**. Ele relata o stride da superfície no membro de **semilargura** do [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no formato de vídeo. Se o filtro upstream não retornar S \_ OK de **QueryAccept**, o VMR rejeitará o formato e tentará se conectar usando o próximo formato anunciado pelo filtro upstream. O VMR anexa o tipo de mídia com o novo formato ao primeiro exemplo de mídia. Após a primeira amostra, o formato permanece constante; o VMR não alternará os formatos enquanto o grafo estiver em execução.

**Renderização de vídeo avançada (EVR)**

O EVR sempre usa o Direct3D para renderização. Se for necessário um stride de superfície maior, o EVR usará o mesmo mecanismo **QueryAccept** que o VMR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[QueryAccept (upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



