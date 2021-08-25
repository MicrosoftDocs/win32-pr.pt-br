---
title: Dados de entrada e saída
description: Dados de entrada e saída
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player plug-ins, entrada e saída de dados
- plug-ins, entrada e saída de dados
- plug-ins de processamento de sinal digital, entrada e saída de dados
- Plug-ins do DSP, entrada e saída de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31e7c6fba24451d65e59c3fb9f56ec6b1413be3d595530414c25c52964b9b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863666"
---
# <a name="data-input-and-output"></a>Dados de entrada e saída

Windows Media Player fornece dados de áudio ou vídeo para plug-ins DSP por meio de um buffer de entrada alocado por Windows Media Player. Os plug-ins DSP retornam dados processados para Windows Media Player por meio de um buffer de saída que também é alocado por Windows Media Player. Windows Media Player gerencia o processo de passagem de dados entre si e o plug-in DSP chamando métodos implementados pelo plug-in. Para um plug-in que atua como um objeto de mídia directX (DMO), o processo funciona da seguinte maneira:

1.  Windows Media Player chama **IMediaObject::P rocessInput,** passando um ponteiro para um objeto **IMediaBuffer** para o plug-in DSP.
2.  O plug-in DSP mantém uma contagem de referência no objeto de buffer de entrada. O plug-in DSP retorna um **HRESULT** de êxito ou falha apropriado.
3.  Windows Media Player chama **IMediaObject::P rocessOutput** DMO, passando um ponteiro para uma matriz de estruturas **\_ DE \_ \_ BUFFER** de DADOS DE SAÍDA (que contêm buffers de saída) para o plug-in DSP.
4.  O plug-in DSP processa os dados no buffer de entrada e copia os dados para o buffer de saída apropriado. O plug-in DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados. Em seguida, o plug-in do DSP retorna um **HRESULT de êxito ou falha apropriado.**
5.  Windows Media Player renderiza o conteúdo no buffer de saída.

Para um plug-in que atua como uma transformação Media Foundation (MFT), o processo funciona da seguinte maneira:

-   Windows Media Player chama **IMFTransform::P rocessInput,** passando um ponteiro para um objeto de interface **IMFSample** para o plug-in DSP.
    1.  O plug-in DSP mantém uma contagem de referência na interface **IMFSample.** O plug-in DSP retorna um **HRESULT** de êxito ou falha apropriado.
    2.  Windows Media Player chama **IMFTransform::P rocessOutput,** passando um ponteiro para uma matriz de estruturas de **\_ \_ \_ BUFFER** de DADOS DE SAÍDA MFT (que contêm buffers de saída) para o plug-in DSP.
    3.  O plug-in DSP processa os dados no buffer de entrada e copia os dados para o buffer de saída apropriado. O plug-in DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados. Em seguida, o plug-in do DSP retorna um **HRESULT de êxito ou falha apropriado.**
    4.  Windows Media Player renderiza o conteúdo no buffer de saída.

Esse processo se repete continuamente enquanto o plug-in está habilitado e Windows Media Player tem conteúdo para renderizar.

> [!Note]  
> Não escreva código que grava dados no buffer de entrada ou lê dados do buffer de saída. O acesso incorreto a buffers de dados pode gerar resultados inesperados.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor do plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




