---
description: Propriedades de codificação
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Propriedades de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743488"
---
# <a name="encoding-properties"></a>Propriedades de codificação

Os Windows áudio de mídia Windows os codificadores de vídeo de mídia do Windows suportam uma variedade de modos de codificação. Esses modos geralmente são configurados definindo propriedades no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT). Para executar a codificação de arquivo, seja usando componentes no nível do WMContainer ou criando uma topologia parcial, você deve configurar o codificador adequadamente definindo propriedades dependendo do modo de codificação e do tipo de mídia do fluxo. O mesmo conjunto de propriedades deve ser definido no codificador e no objeto (sink de arquivo ASF ou multiplexador ASF) que você está usando para gravar o arquivo ASF.

As propriedades do codificador são definidas em wmcodecdsp.h. As propriedades específicas usadas para configurar o codificador são definidas usando os métodos da interface [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

-   [Propriedades de fluxo de áudio](#audio-stream-properties)
-   [Propriedades do fluxo de vídeo](#video-stream-properties)
-   [Configurando o código do codificador Repositório de Propriedades](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Propriedades de fluxo de áudio

A tabela a seguir mostra as configurações do codificador para um fluxo de áudio.



| Tipo de codificação                                                                                        | Nome da propriedade – Valor                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED – **FALSE** (opcional)Por padrão, MFPKEY \_ VBRENABLED é definido como **FALSE.**<br/>                                                                                             |
| [Codificação de taxa de bits de variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 1 (opcional)<br/> Por padrão, MFPKEY \_ PASSESUSED é definido como 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY – de 0 a 100<br/> |
| [Codificação de taxa de bits de variável irr pouco restrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 2<br/>                                                                                                                          |
| [Codificação de taxa de bits de variável restrita de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 2<br/> MFPKEY \_ RMAX – Taxa de bits máxima<br/> MFPKEY \_ BMAX – Janela de buffer máxima<br/>                               |



 

### <a name="video-stream-properties"></a>Propriedades do fluxo de vídeo

A tabela a seguir mostra as configurações do codificador para um fluxo de vídeo.



| Tipo de codificação                                                                                        | Nome da propriedade                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED – **FALSE** (opcional)<br/> Por padrão, MFPKEY \_ VBRENABLED é definido como **FALSE.**<br/> MFPKEY \_ VIDEOWINDOW – janela buffer<br/>                                  |
| [Codificação de taxa de bits de variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 1 (opcional)<br/> Por padrão, MFPKEY \_ PASSESUSED é definido como 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY – de 0 a 100<br/> |
| [Codificação de taxa de bits de variável irr pouco restrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 2<br/>                                                                                                                          |
| [Codificação de taxa de bits de variável restrita de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 2<br/> MFPKEY \_ RMAX – Taxa de bits máxima<br/> MFPKEY \_ BMAX – Janela de buffer máxima<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configurando o código do codificador Repositório de Propriedades

Você deve configurar um codificador especificando o tipo de codificação e as várias configurações específicas do fluxo antes da sessão de codificação. Você também deve definir as propriedades do codificador no armazenamento de propriedades de um objeto [ContentInfo ASF](asf-contentinfo-object.md) que representa o objeto de título ASF do arquivo de saída.

Se você estiver usando um codificador MFT:

1.  Obter uma referência à interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do codificador MFT, conforme descrito em Usando [a interface IMFTransform](using-an-encoder-s-imftransform--interface.md)de um codificador.
2.  Consultando o MFT do codificador para a interface **IPropertyStore.**
3.  Definindo as propriedades necessárias chamando **IPropertyStore::SetValue**.

Se você estiver usando os objetos de ativação do codificador integrado e já tiver criado um configurado no sink do arquivo ASF, poderá passar o armazenamento de propriedades do sink de mídia do ASF para [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). O codificador é configurado automaticamente com base nas configurações especificadas pelo aplicativo. Para obter mais informações, consulte o procedimento descrito em [Usando objetos de ativação de um codificador.](using-an-encoder-s-activation-objects.md)

Para obter mais informações sobre como criar objetos Media Foundation usando objetos de ativação, consulte [Objetos de ativação](activation-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inciando um MFT codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 
