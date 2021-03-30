---
description: Tipos de codificação ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificação ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089800"
---
# <a name="asf-encoding-types"></a>Tipos de codificação ASF

Todos os métodos de codificação se concentram no buffer usado pelo codificador para gerenciar dados de entrada não compactados. Esse buffer é definido pela taxa de bits do fluxo, em bits por segundo, e pela janela de buffer, em milissegundos. Ao codificar para arquivos ASF, os codificadores de mídia do Windows obedecem às restrições do buffer. Para obter mais informações sobre a janela de buffer, consulte [o modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md). Saber como e quando usar cada método pode ajudá-lo a criar conteúdo compactado de alta qualidade. A tabela a seguir contém links para tópicos sobre cada um dos métodos de codificação disponíveis que um aplicativo pode usar para codificar dados de mídia para o ASF.



| Método de codificação                                                                                      | Descrição                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | O codificador compacta os dados a uma taxa de bits especificada.                                                                                                                                                     |
| [Codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | O codificador compacta os dados a um valor de qualidade específico para que a qualidade da mídia codificada seja consistente durante sua duração, independentemente dos requisitos de buffer do fluxo resultante. |
| [Codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | O codificador compacta os dados à qualidade mais alta possível, mantendo uma taxa de bits especificada. Esse modo também é chamado de codificação de taxa de bits variável (VBR) de 2 passagens.                                    |
| [Codificação de taxa de bits de variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | O codificador compacta os dados a uma taxa de bits especificada enquanto mantém os valores de buffer na janela e na taxa de bits do buffer máximo especificados. Esse modo também é chamado de taxa de bits de pico de 2 passagens.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 



