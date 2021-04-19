---
description: A codificação de duas passagens pode ser usada para a taxa de bits constante (CBR) e para a codificação de taxa de bits variável (VBR) com alguns dos codecs de mídia do Windows.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Usando a codificação Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782971"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Usando a codificação Two-Pass (Microsoft Media Foundation)

A codificação de duas passagens pode ser usada para a taxa de bits constante (CBR) e para a codificação de taxa de bits variável (VBR) com alguns dos codecs de mídia do Windows. Você pode encontrar o número máximo de passagens de codificação com suporte por um codec recuperando a propriedade [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) . Nenhum dos codecs dá suporte a mais de duas passagens. Configure o DMO para usar duas passagens definindo a propriedade [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) como 2.

Entregue os exemplos ao codificador DMO, um de cada vez, como você faria em um modo de passagem única. Quando você processa os exemplos de entrada para sua passagem de pré-processamento, as chamadas para [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) ou [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) retornará **S \_ false**, para indicar que nenhuma saída é produzida.

No final da primeira passagem (após a última entrada ser processada pela primeira vez), você deve definir a propriedade [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) para notificar o codec de que a próxima entrada processada é a primeira entrada da segunda passagem. Nenhum valor é necessário para essa propriedade, portanto, você deve usar uma estrutura **Variant** vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 
