---
description: Esta seção descreve como configurar fluxos VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usando a codificação VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a9e1a61baf0539c0597e68f24dfad1496918012e52f778a1b7a64de27e5faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871225"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Usando a codificação VBR (Microsoft Media Foundation)

Conforme detalhado no [](encodingmethods.md) tópico Métodos de Codificação, a codificação VBR (taxa de bits variável) é usada para melhorar a consistência da qualidade do conteúdo. Você configura fluxos VBR da mesma maneira que codifica fluxos CBR (taxa de bits constante), exceto para os parâmetros de buffer (taxa de bits e janela de buffer). Esta seção descreve como configurar fluxos VBR.

## <a name="configuring-quality-based-vbr"></a>Configurando a VBR baseada em qualidade

A codificação usando o método VBR baseado em qualidade não requer nenhum parâmetro de buffer predefinido. Em vez disso, você especifica um nível de qualidade (de 0 a 100) que o codificador usa para determinar os parâmetros de buffer apropriados dinamicamente. Esse modo de codificação usa apenas uma passagem de codificação.

Você pode enumerar os tipos de saída VBR baseados em qualidade com suporte para os codecs de áudio. Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída. Para obter mais informações, [consulte Enumerando tipos de áudio para modos de codificação específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar um fluxo de vídeo VBR baseado em qualidade, você deve definir as propriedades listadas na tabela a seguir.



| Propriedade                                            | Descrição                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Definido como VARIANT \_ TRUE.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | De acordo com o valor de qualidade desejado, de 0 a 100. Nem todos os valores de qualidade representam configurações discretas. Consulte a descrição da propriedade para obter mais informações. |



 

## <a name="configuring-unconstrained-vbr"></a>Configurando o VBR irr pouco restrito

A codificação VBR irr pouco restrita permite que o codificador varie o tamanho das amostras individuais sem nenhum limite de buffer explícito. No entanto, a taxa média de bits durante a duração do conteúdo resultante deve ser menor ou igual ao valor especificado. A VBR irr pouco restrita requer duas passagens de codificação.

Você pode enumerar os tipos de saída VBR de duas passs com suporte para os codecs de áudio. Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída. Para obter mais informações, [consulte Enumerando tipos de áudio para modos de codificação específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar um fluxo de vídeo VBR irr pouco restrito, você deve definir as propriedades listadas na tabela a seguir.



| Propriedade                                            | Descrição                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Definido como VARIANT \_ TRUE.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | De definido como 2.                            |
| [MFPKEY \_ LTDG](mfpkey-ravgproperty.md)             | De acordo com a taxa de bits média desejada. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configurando Peak-Constrained VBR

A VBR com restrição de pico é como uma VBR irr pouco restrita, já que ela é limitada a uma taxa média de bits durante a duração do fluxo. Além disso, o VBR com restrição de pico está em conformidade com um buffer de pico. Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico, assim como um buffer CBR é descrito por uma taxa média de bits e uma janela de buffer. Esse modo fornece a flexibilidade do codificador em como ele codifica amostras individuais enquanto adere às limitações de pico. Isso é particularmente útil quando a decodificação é executada por um chip em um dispositivo, como um player de DVD, em que há limitações de hardware que devem ser consideradas.

Os tipos de saída do codificador de áudio VBR com restrição de pico com suporte são os mesmos tipos enumerados para VBR irr pouco restrita. De definidos os valores de pico no DMO e use o tipo entregue. Para obter mais informações, [consulte Enumerando tipos de áudio para modos de codificação específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar um fluxo de vídeo VBR com restrição de pico, você deve definir as propriedades listadas na tabela a seguir usando o método **IPropertyBag::Write.**



| Propriedade                                            | Descrição                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Definido como VARIANT \_ TRUE.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | De definido como 2.                                                       |
| [MFPKEY \_ LTDG](mfpkey-ravgproperty.md)             | De acordo com a taxa de bits média desejada.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | De acordo com a taxa de bits de pico desejada.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | De acordo com a janela de buffer que corresponde à taxa de bits de pico. |



 

> [!Note]  
> É recomendável definir a taxa de bits de pico como pelo menos duas vezes a taxa média de bits. Definir a taxa de pico como um valor mais baixo pode fazer com que o codec codije o conteúdo como CBR de duas passs em vez de VBR com restrição de pico.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> <dt>

[Usando Two-Pass codificação](usingtwoencodingpasses.md)
</dt> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



