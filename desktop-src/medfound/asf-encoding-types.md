---
description: Tipos de codificação ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificação ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83e1b9f39118cea5e7c5610b9480ea3d615a002d7f889933e3f3e7d62f0b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035574"
---
# <a name="asf-encoding-types"></a>Tipos de codificação ASF

Todos os métodos de codificação se concentram no buffer usado pelo codificador para gerenciar dados de entrada descompactados. Esse buffer é definido pela taxa de bits do fluxo, em bits por segundo, e pela janela do buffer, em milissegundos. Ao codificar para arquivos ASF, os codificadores Windows Media obedecem às restrições do buffer. Para obter mais informações sobre a janela de buffer, consulte [O modelo de buffer de bucket vazado](the-leaky-bucket-buffer-model.md). Saber como e quando usar cada método pode ajudá-lo a criar conteúdo compactado de alta qualidade. A tabela a seguir contém links para tópicos sobre cada um dos métodos de codificação disponíveis que um aplicativo pode usar para codificar dados de mídia para ASF.



| Método de codificação                                                                                      | Descrição                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | O codificador compacta dados para uma taxa de bits especificada.                                                                                                                                                     |
| [Codificação de taxa de bits de variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | O codificador compacta dados para um valor de qualidade específico para que a qualidade da mídia codificada seja consistente durante toda a sua duração, independentemente dos requisitos de buffer do fluxo resultante. |
| [Codificação de taxa de bits de variável irr pouco restrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | O codificador compacta os dados para a mais alta qualidade possível, mantendo uma taxa de bits especificada. Esse modo também é chamado de codificação de VBR (taxa de bits variável) de duas passes.                                    |
| [Codificação de taxa de bits de variável restrita de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | O codificador compacta dados para uma taxa de bits especificada, mantendo os valores de buffer sob a janela de buffer máxima especificada e a taxa de bits. Esse modo também é chamado de VBR de pico de duas passs.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF em Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 



