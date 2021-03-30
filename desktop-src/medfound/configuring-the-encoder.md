---
description: Propriedades de codificação
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Propriedades de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 093b72dc37501ca88882c6e3b530cda0eed1baa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089774"
---
# <a name="encoding-properties"></a>Propriedades de codificação

Os codificadores de vídeo de áudio do Windows e Windows Media oferecem suporte a uma variedade de modos de codificação. Esses modos geralmente são configurados definindo propriedades no codificador [Media Foundation transformação](media-foundation-transforms.md) (MFT). Para executar a codificação de arquivo, seja usando componentes de nível de WMContainer ou criando uma topologia parcial, você deve configurar o codificador adequadamente definindo as propriedades dependendo do modo de codificação e do tipo de mídia do fluxo. O mesmo conjunto de propriedades deve ser definido no codificador e no objeto (coletor de arquivo ASF ou multiplexador ASF) que você está usando para gravar o arquivo ASF.

As propriedades do codificador são definidas em wmcodecdsp. h. As propriedades específicas que são usadas para configurar o codificador são definidas usando os métodos da interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

-   [Propriedades do fluxo de áudio](#audio-stream-properties)
-   [Propriedades de fluxo de vídeo](#video-stream-properties)
-   [Configurando o armazenamento de propriedades do codificador](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Propriedades do fluxo de áudio

A tabela a seguir mostra as configurações do codificador para um fluxo de áudio.



| Tipo de codificação                                                                                        | Nome da propriedade-valor                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (opcional) por padrão, MFPKEY \_ VBRENABLED é definido como **false**.<br/>                                                                                             |
| [Codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (opcional)<br/> Por padrão, MFPKEY \_ PASSESUSED é definido como 1.<br/> MFPKEY \_ desired \_ VBRQUALITY-de 0 a 100<br/> |
| [Codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codificação de taxa de bits de variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-taxa de bits máxima<br/> MFPKEY \_ BMAX-janela de buffer máximo<br/>                               |



 

### <a name="video-stream-properties"></a>Propriedades de fluxo de vídeo

A tabela a seguir mostra as configurações do codificador para um fluxo de vídeo.



| Tipo de codificação                                                                                        | Nome da propriedade                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificação de taxa de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (opcional)<br/> Por padrão, MFPKEY \_ VBRENABLED é definido como **false**.<br/> \_Janela MFPKEY VIDEOWINDOW-buffer<br/>                                  |
| [Codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (opcional)<br/> Por padrão, MFPKEY \_ PASSESUSED é definido como 1.<br/> MFPKEY \_ desired \_ VBRQUALITY-de 0 a 100<br/> |
| [Codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codificação de taxa de bits de variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-taxa de bits máxima<br/> MFPKEY \_ BMAX-janela de buffer máximo<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configurando o armazenamento de propriedades do codificador

Você deve configurar um codificador especificando o tipo de codificação e as várias configurações específicas de fluxo antes da sessão de codificação. Você também deve definir as propriedades do codificador no repositório de propriedades de um [objeto ASF ContentInfo](asf-contentinfo-object.md) que representa o objeto de cabeçalho ASF do arquivo de saída.

Se você estiver usando um MFT do codificador:

1.  Obtenha uma referência à interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do MFT do codificador, conforme descrito em [usando a interface IMFTransform de um codificador](using-an-encoder-s-imftransform--interface.md).
2.  Consultando o MFT do codificador para a interface **IPropertyStore** .
3.  Definindo as propriedades necessárias chamando **IPropertyStore:: SetValue**.

Se você estiver usando objetos internos de ativação do codificador e já tiver criado um configurado o coletor de arquivos ASF, poderá passar o repositório de propriedades do coletor de mídia ASF para [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). O codificador é configurado automaticamente com base nas configurações especificadas pelo aplicativo. Para obter mais informações, consulte o procedimento descrito em [usando objetos de ativação de um codificador](using-an-encoder-s-activation-objects.md).

Para obter mais informações sobre como criar objetos de Media Foundation usando objetos de ativação, consulte [objetos de ativação](activation-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 
