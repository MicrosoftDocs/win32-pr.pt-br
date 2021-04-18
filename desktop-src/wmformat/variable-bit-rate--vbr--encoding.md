---
title: Codificação de taxa de bits variável (VBR)
description: Codificação de taxa de bits variável (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- SDK do Windows Media Format, codificação de VBR
- SDK do Windows Media Format, taxa de bits variável (VBR)
- SDK do Windows Media Format, codificação VBR com base na qualidade
- Windows Media Format SDK, codificação de VBR não restringida
- Windows Media Format SDK, codificação de taxa de bits restrita
- codecs, codificação de VBR
- codecs, taxa de bits variável (VBR)
- codecs, codificação de VBR com base na qualidade
- codecs, codificação de VBR não restringida
- codecs, codificação de taxa de bits restrita
- taxa de bits variável (VBR), sobre
- VBR (taxa de bits variável), sobre
- codificação de VBR com base na qualidade, sobre
- codificação de VBR não restringida, sobre
- codificação de taxa de bits restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814452"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Codificação de taxa de bits variável (VBR)

A codificação de taxa de bits variável (VBR) é uma alternativa para a taxa de bits constante (CBR) e é suportada por alguns codecs. Onde a codificação CBR se esforça para manter a taxa de bits da mídia codificada, a VBR busca obter a melhor qualidade possível da mídia codificada.

A qualidade do conteúdo codificado é determinada pela quantidade de dados que é perdida quando o conteúdo é compactado e descompactado. Muitos fatores influenciam a perda de dados no processo de compressão, Porém, em geral, quanto mais complexos forem os dados originais e quanto maior for a taxa de compressão, mais detalhes são perdidos no processo de compactação.

Há três tipos de codificação de VBR: baseada em qualidade, irrestrito e restrito.

## <a name="quality-based-vbr-encoding"></a>Codificação de VBR com base na qualidade

O primeiro tipo de codificação de VBR é baseado em qualidade, que usa uma passagem de codificação. A codificação VBR com base na qualidade permite que você especifique um nível de qualidade para um fluxo de mídia digital em vez de uma taxa de bits. O codec codificará o conteúdo para que todos os exemplos sejam de qualidade comparável.

A principal vantagem da codificação de VBR com base na qualidade é que a qualidade é consistente dentro de um arquivo e de um arquivo para o outro. Por exemplo, você pode escrever um programa para copiar músicas de CD para arquivos ASF em um computador. Nesse caso, a qualidade consistente provavelmente é mais importante para a experiência do usuário final do que o tamanho de arquivo consistente. O uso da codificação VBR com base na qualidade garantiria que todas as músicas copiadas tenham a mesma qualidade.

A desvantagem da codificação de VBR baseada em qualidade é que não há realmente nenhuma maneira de saber os requisitos de tamanho ou largura de banda da mídia codificada antes da codificação. Isso pode tornar arquivos codificados em taxa de bits com base em qualidade inadequados para circunstâncias em que a memória ou largura de banda são restritas, como players de mídia portáteis ou conexões de Internet de baixa largura de banda.

Em geral, a codificação VBR com base na qualidade é adequada para a reprodução local ou conexões de rede de largura de banda alta. Nesses casos, a qualidade consistente oferecerá uma melhor experiência do usuário.

## <a name="unconstrained-vbr-encoding"></a>Codificação de VBR não restringida

A codificação de VBR não restringida usa duas passagens de codificação. Ao usar a codificação VBR não restringida, você especifica uma taxa de bits para o fluxo, como você faria com a codificação de CBR. No entanto, o codec usa esse valor somente como a taxa de bits média para o fluxo e codifica para que a qualidade seja a mais alta possível, mantendo a média. A taxa de bits real em qualquer ponto no fluxo codificado pode variar muito do valor médio.

Você não define uma janela de buffer para a codificação de taxa de bits não restringida como faria para um fluxo codificado em CBR. Em vez disso, o codec computa o tamanho da janela de buffer necessária com base nos requisitos dos exemplos codificados.

A vantagem da codificação de VBR não restringida é que o fluxo compactado tem a melhor qualidade possível enquanto permanece dentro de uma largura de banda média previsível.

## <a name="constrained-vbr-encoding"></a>Codificação de taxa de bits restrita

A codificação de taxa de bits restrita é idêntica à codificação VBR não restrita, exceto pelo fato de que você especifica uma taxa de bit máxima e uma janela de buffer máximo no perfil. Em seguida, o codec usa os valores máximos para determinar como compactar os dados. Se você definir os valores máximos como alto o suficiente, a codificação de taxa de bits restrita produzirá o mesmo fluxo codificado como codificação de VBR não restrita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escolhendo um método de codificação**](choosing-an-encoding-method.md)
</dt> <dt>

[**Recursos do codec**](codec-features.md)
</dt> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> <dt>

[**Configurando fluxos de VBR**](configuring-vbr-streams.md)
</dt> <dt>

[**Codificação de taxa de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codificação de duas passagens**](two-pass-encoding.md)
</dt> <dt>

[**Usando a codificação Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




