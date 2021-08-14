---
title: Two-Pass codificação
description: Two-Pass codificação
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows SDK de Formato de Mídia, codificação de duas passs
- Windows SDK de Formato de Mídia, codificação de 2 pass
- codecs, codificação de duas passs
- codecs,codificação de 2 pass
- codificação de duas passs, sobre
- Codificação de duas passs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845334"
---
# <a name="two-pass-encoding"></a>Two-Pass codificação

A codificação de duas passs é um método de codificação disponível com alguns codecs, como o codec Windows Media Video 9. Quando você usa a codificação de duas passões, o codec processa todos os exemplos para o fluxo duas vezes. Na primeira passagem, o codec coleta informações sobre o conteúdo do fluxo. Na segunda passagem, o codec usa as informações coletadas na primeira passagem para otimizar o processo de codificação para o fluxo.

No modo de codificação Taxa de Bits Constante, os arquivos codificados em duas passagens geralmente são mais eficientes do que os arquivos codificados em uma única passagem. A VBR baseada em qualidade, que é uma passagem, produz uma qualidade mais consistente do que a VBR baseada em taxa de bits, que é de duas pass.

Não é possível usar a codificação de duas passões em transmissões ao vivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos do Codec**](codec-features.md)
</dt> <dt>

[**Usando Two-Pass codificação**](using-two-pass-encoding.md)
</dt> </dl>

 

 




