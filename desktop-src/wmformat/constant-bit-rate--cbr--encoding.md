---
title: Codificação de taxa de bits constante (CBR)
description: Codificação de taxa de bits constante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- SDK do Windows Media Format, codificação de CBR
- SDK do Windows Media Format, taxa de bits constante (CBR)
- codecs, codificação de CBR
- codecs, taxa de bits constante (CBR)
- taxa de bits constante (CBR)
- CBR (taxa de bits constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364349"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Codificação de taxa de bits constante (CBR)

A codificação de taxa de bits constante (CBR) é o método padrão de codificação com o Windows Media Format SDK. Ao usar a codificação de CBR, você especifica a taxa de bits de destino para um fluxo e o codec usa qualquer quantidade de compactação necessária para obtê-la.

Com a codificação CBR, a taxa de bits e o tamanho do fluxo codificado são conhecidos antes da codificação. Por exemplo, se você estiver codificando uma música de três minutos a 32.000 bits por segundo, saberá que o tamanho do arquivo será de cerca de 704 quilobytes (32.000 bps x 180 segundos/8 bits por byte/1.024). Você também sabe que a largura de banda necessária para transmitir o conteúdo codificado é de cerca de 32.000 bits por segundo.

A codificação de taxa de bits de variável restrita (descrita na seção a seguir) também permite que você saiba a taxa de bits antes da codificação, mas como a taxa é variável, o arquivo resultante não pode ser transmitido com eficiência como um arquivo codificado no modo CBR. Com a CBR, a taxa de bits ao longo do tempo sempre permanece próxima à taxa de bits média ou de destino, e a quantidade de variação pode ser especificada.

A desvantagem da codificação CBR é que a qualidade do conteúdo codificado não será constante. Como algum conteúdo é mais difícil de ser compactado, partes de um fluxo de CBR serão de menor qualidade do que outras. Por exemplo, um filme típico tem algumas cenas que são razoavelmente estáticas e algumas cenas que estão cheias de ação. Se você codificar um filme usando CBR, os bastidores estáticos e, portanto, fáceis de codificar com eficiência, serão de maior qualidade do que as cenas de ação, que são muito mais difíceis de codificar com eficiência.

A codificação de CBR também pode resultar em uma qualidade inconsistente de um arquivo para outro. Se você usar a CBR para codificar várias músicas de diferentes gêneros na mesma taxa de bits, poderá notar alguma diferença na qualidade entre elas.

Em geral, as variações na qualidade de um arquivo CBR são mais pronunciadas em taxas de bits inferiores. Em taxas de bits mais altas, a qualidade de um arquivo codificado em CBR ainda variará, mas os problemas de qualidade serão menos perceptíveis para o usuário. Ao usar a codificação de CBR, você deve definir a largura de banda tão alta quanto o cenário de entrega permitir.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escolhendo um método de codificação**](choosing-an-encoding-method.md)
</dt> <dt>

[**Recursos do codec**](codec-features.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




