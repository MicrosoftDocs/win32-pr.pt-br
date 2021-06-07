---
title: Para enumerar formatos de codec
description: Para enumerar formatos de codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- fluxos, enumerando formatos de codec
- codecs, enumerações
- fluxos, formatos de codec
- codecs, formatos
- codecs, interface IWMCodecInfo
- IWMCodecInfo, formatos de codec
- codecs, interface IWMCodecInfo3
- IWMCodecInfo3, formatos de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444777"
---
# <a name="to-enumerate-codec-formats"></a>Para enumerar formatos de codec

Um formato de codec é um objeto de configuração de fluxo populado com dados de um codec. Cada formato de codec contém uma configuração de mídia com suporte do codec. A maioria dos codecs de áudio dá suporte a um número finito de formatos, cada um dos quais é enumerado pelo codec e pode ser acessado usando os métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). Os codecs de vídeo, por outro lado, fornecem apenas um único formato. Isso ocorre porque os fluxos de vídeo têm variáveis, como tamanho de quadro, que são mais flexíveis do que as configurações de um fluxo de áudio. Com um fluxo de vídeo, você deve preencher alguns dos valores de configuração de fluxo; as configurações de fluxo de áudio só devem ser editadas para atribuir um nome, um nome de conexão e um número de fluxo. Para obter mais informações, consulte [configuração comum a todos os fluxos](configuration-common-to-all-streams.md).

Os formatos de codec enumerados dependem das configurações atuais de enumeração do codec, que são definidas usando [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Atualmente, há suporte apenas para duas propriedades de codec: g \_ wszNumPasses, que especifica o número de passagens de codificação que o codec executará e g \_ wszVBREnabled, que especifica se o codec usará a codificação de taxa de bits variável. O número máximo de passagens de codificação com suporte de qualquer um dos codecs é dois, portanto, há quatro configurações distintas para as quais você pode recuperar codecs, conforme mostrado na tabela a seguir.



|    &nbsp;    | Fluxo de taxa de bits constante (CBR) | 2-transmitir fluxo de CBR | Fluxo de taxa de bits variável (VBR) com base na qualidade | Fluxo de VBR (restrito ou irrestrito) com base na taxa de bits |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Para enumerar os formatos com suporte para um codec, use [**IWMCodecInfo:: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) para localizar o número de codecs com suporte. Em seguida, chame [**IWMCodecInfo:: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) para cada formato. O formato indexa o intervalo de zero, para um menor que o número total de formatos com suporte. Você pode recuperar uma descrição do formato chamando [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Ao usar **GetCodecFormatDesc**, você não precisa usar **GetCodecFormat**, porque o objeto de configuração de fluxo é recuperado por ambos os métodos. Os formatos de codec de vídeo não incluem uma descrição. Cada codec de vídeo tem apenas um formato que é usado para todos os fluxos desse tipo.

Ao recuperar um formato de codec, você obtém a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de um objeto de configuração de fluxo que contém as configurações de formato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo informações de configuração de fluxo de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




