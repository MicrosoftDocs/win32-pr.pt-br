---
description: Mostra como gravar um decodificador para Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Exemplo de decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920630"
---
# <a name="decoder-sample"></a>Exemplo de decodificador

Mostra como gravar um decodificador para Microsoft Media Foundation.

Este exemplo implementa um decodificador de vídeo MPEG-1 simulado que exibe o código de tempo para cada quadro de vídeo. Na verdade, ele não decodificará o fragmentado MPEG-1. A imagem a seguir mostra a saída de vídeo do decodificador.

![captura de tela de um quadro de vídeo do decodificador](images/decodersample.png)

> [!Note]  
> Antes do SDK do Windows para o Windows 7, esse exemplo foi incluído como parte do [exemplo de MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



