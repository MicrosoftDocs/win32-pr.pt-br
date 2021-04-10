---
description: Esta seção descreve como configurar fluxos de VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usando a codificação de VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164879"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Usando a codificação de VBR (Microsoft Media Foundation)

Conforme detalhado no tópico [métodos de codificação](encodingmethods.md) , a codificação taxa de bits variável (VBR) é usada para melhorar a consistência da qualidade do conteúdo. Configure fluxos de VBR da mesma maneira que você codifica fluxos de taxa de bits constante (CBR), exceto para os parâmetros de buffer (taxa de bits e janela de buffer). Esta seção descreve como configurar fluxos de VBR.

## <a name="configuring-quality-based-vbr"></a>Configuração da VBR com base na qualidade

A codificação usando o método de taxa de bits baseada em qualidade não requer nenhum parâmetro de buffer predefinido. Em vez disso, você especifica um nível de qualidade (de 0 a 100) que o codificador usa para determinar os parâmetros de buffer apropriados dinamicamente. Esse modo de codificação usa apenas uma passagem de codificação.

Você pode enumerar os tipos de saída de VBR com base em qualidade com suporte para os codecs de áudio. Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída. Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar um fluxo de vídeo VBR com base na qualidade, você deve definir as propriedades listadas na tabela a seguir.



| Propriedade                                            | Descrição                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Defina como VARIANT \_ true.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Defina para o valor de qualidade desejado, de 0 a 100. Nem todos os valores de qualidade representam configurações discretas. Consulte a descrição da propriedade para obter mais informações. |



 

## <a name="configuring-unconstrained-vbr"></a>Configurando a VBR não restringida

A codificação de VBR não restringida permite que o codificador varie o tamanho de amostras individuais sem nenhum limite de buffer explícito. No entanto, a taxa média de bits sobre a duração do conteúdo resultante deve ser menor ou igual ao valor especificado. A VBR não restringida requer duas passagens de codificação.

Você pode enumerar os tipos de saída de VBR de dois passos com suporte para os codecs de áudio. Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída. Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar um fluxo de vídeo de taxa de bits variável irrestrita, você deve definir as propriedades listadas na tabela a seguir.



| Propriedade                                            | Descrição                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Defina como VARIANT \_ true.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Defina como 2.                            |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Defina para a taxa de bits média desejada. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configurando Peak-Constrained VBR

A VBR com restrição de pico é como uma VBR não restrita, pois ela é confinada a uma taxa média de bits durante a duração do fluxo. Além disso, a taxa de bits com restrição de pico está em conformidade com um buffer de pico. Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico, assim como um buffer de CBR é descrito por uma taxa média de bits e uma janela de buffer. Esse modo fornece a flexibilidade do codificador em como ele codifica exemplos individuais enquanto obedece às limitações de pico. Isso é particularmente útil quando a decodificação é executada por um chip em um dispositivo, como um DVD Player, onde há limitações de hardware que devem ser consideradas.

Os tipos de saída do codificador de áudio VBR e com restrição de pico têm os mesmos tipos enumerados para a VBR não restrita. Defina os valores de pico no DMO e use o tipo entregue. Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar um fluxo de vídeo VBR com restrição de pico, você deve definir as propriedades listadas na tabela a seguir usando o método **IPropertyBag:: Write** .



| Propriedade                                            | Descrição                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Defina como VARIANT \_ true.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Defina como 2.                                                       |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Defina para a taxa de bits média desejada.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | Defina para a taxa de bits de pico desejada.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | Defina para a janela de buffer que corresponde à taxa de bits de pico. |



 

> [!Note]  
> É recomendável que você defina a taxa de bits de pico para pelo menos duas vezes a taxa média de bits. Definir a taxa de pico para um valor mais baixo pode fazer com que o codec Codifique o conteúdo como CBR de duas passagens em vez da taxa de bits de pico restrita.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> <dt>

[Usando a codificação Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



