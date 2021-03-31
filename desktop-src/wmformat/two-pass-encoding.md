---
title: Codificação de Two-Pass
description: Codificação de Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codificação em duas passagens
- SDK de formato de mídia do Windows, codificação de 2 passagens
- codecs, codificação em duas passagens
- codecs, codificação de 2 passagens
- codificação de dois passos, sobre
- 2-passar codificação, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005278"
---
# <a name="two-pass-encoding"></a>Codificação de Two-Pass

Codificação de duas passagens é um método de codificação disponível com alguns codecs, como o codec do Windows Media Video 9. Quando você usa codificação de duas passagens, o codec processa todos os exemplos para o fluxo duas vezes. Na primeira passagem, o codec reúne informações sobre o conteúdo do fluxo. Na segunda passagem, o codec usa as informações coletadas na primeira passagem para otimizar o processo de codificação para o fluxo.

No modo de codificação de taxa de bits constante, os arquivos codificados em duas passagens geralmente são mais eficientes do que os arquivos codificados em uma única passagem. A taxa de bits baseada em qualidade, que é uma passagem, produz uma qualidade mais consistente do que a VBR baseada em taxa de bits, que é de duas passagens.

Não é possível usar codificação de duas passagens em transmissões ao vivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos do codec**](codec-features.md)
</dt> <dt>

[**Usando a codificação Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




