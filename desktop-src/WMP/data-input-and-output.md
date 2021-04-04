---
title: Dados de entrada e saída
description: Dados de entrada e saída
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-ins do Windows Media Player, entrada e saída de dados
- plug-ins, entrada e saída de dados
- plug-ins de processamento de sinal digital, entrada e saída de dados
- Plug-ins do DSP, entrada e saída de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084083"
---
# <a name="data-input-and-output"></a>Dados de entrada e saída

O Windows Media Player fornece dados de áudio ou vídeo para plug-ins DSP por meio de um buffer de entrada alocado pelo Windows Media Player. Plug-ins do DSP retornam dados processados para o Windows Media Player por meio de um buffer de saída que também é alocado pelo Windows Media Player. O Windows Media Player gerencia o processo de passagem de dados entre si mesmo e o plug-in DSP chamando métodos implementados pelo plug-in. Para que um plug-in atue como um DMO (objeto de mídia do DirectX), o processo funciona da seguinte maneira:

1.  O Windows Media Player chama **IMediaObject::P rocessinput**, passando um ponteiro para um objeto **IMediaBuffer** para o plug-in do DSP.
2.  O plug-in do DSP mantém uma contagem de referência no objeto de buffer de entrada. O plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.
3.  O Windows Media Player chama **IMediaObject::P rocessoutput**, passando um ponteiro para uma matriz de estruturas de buffer de dados de saída do DMO (que contêm buffers de saída) para o plug-in do DSP. **\_ \_ \_**
4.  O plug-in do DSP processa os dados no buffer de entrada e, em seguida, copia os dados para o buffer de saída apropriado. O plug-in do DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados. Em seguida, o plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.
5.  O Windows Media Player renderiza o conteúdo no buffer de saída.

Para que um plug-in atue como uma Media Foundation transformação (MFT), o processo funciona da seguinte maneira:

-   O Windows Media Player chama **IMFTransform::P rocessinput**, passando um ponteiro para um objeto de interface **IMFSample** para o plug-in do DSP.
    1.  O plug-in do DSP mantém uma contagem de referência na interface **IMFSample** . O plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.
    2.  O Windows Media Player chama **IMFTransform::P rocessoutput**, passando um ponteiro para uma matriz de estruturas de buffer de dados de saída da MFT (que contêm buffers de saída) para o plug-in do DSP. **\_ \_ \_**
    3.  O plug-in do DSP processa os dados no buffer de entrada e, em seguida, copia os dados para o buffer de saída apropriado. O plug-in do DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados. Em seguida, o plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.
    4.  O Windows Media Player renderiza o conteúdo no buffer de saída.

Esse processo se repete continuamente enquanto o plug-in está habilitado e o Windows Media Player tem conteúdo a ser renderizado.

> [!Note]  
> Não escreva código que grave dados no buffer de entrada ou leia dados do buffer de saída. O acesso incorreto aos buffers de dados pode gerar resultados inesperados.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




