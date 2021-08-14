---
title: Para enumerar formatos codec
description: Para enumerar formatos codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- fluxos, enumerando formatos de codec
- codecs,enumerações
- fluxos, formatos de codec
- codecs,formats
- codecs, interface IWMCodecInfo
- IWMCodecInfo, formatos de codec
- codecs, interface IWMCodecInfo3
- IWMCodecInfo3, formatos de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221b675c5aa3b5602bcfda96b22233f77d4ba92199f29f36885a4053700dfd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196512"
---
# <a name="to-enumerate-codec-formats"></a>Para enumerar formatos codec

Um formato codec é um objeto de configuração de fluxo populado com dados de um codec. Cada formato de codec contém uma configuração de mídia com suporte pelo codec. A maioria dos codecs de áudio dá suporte a um número finito de formatos, cada um dos quais é enumerado pelo codec e pode ser acessado usando os métodos [**de IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). Codecs de vídeo, por outro lado, fornecem apenas um único formato. Isso porque os fluxos de vídeo têm variáveis, como o tamanho do quadro, que são mais flexíveis do que as configurações de um fluxo de áudio. Com um fluxo de vídeo, você deve preencher alguns dos valores de configuração de fluxo; As configurações de fluxo de áudio só devem ser editadas para atribuir um nome, um nome de conexão e um número de fluxo. Para obter mais informações, consulte [Configuração comum para todos Fluxos](configuration-common-to-all-streams.md).

Os formatos de codec enumerados dependem das configurações de enumeração de codec atuais, que são definidas usando [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Atualmente, há suporte para apenas duas propriedades codec: g wszNumPasses, que especifica o número de passagens de codificação que o codec executará e \_ g wszVBREnabled, que especifica se o codec usará a codificação de taxa de bits \_ variável. O número máximo de passagens de codificação com suporte por qualquer um dos codecs é dois, portanto, há quatro configurações distintas para as quais você pode recuperar codecs, conforme mostrado na tabela a seguir.



|    &nbsp;    | Fluxo de CBR (taxa de bits constante) | Fluxo CBR de duas passs | Fluxo de VBR (taxa de bits variável) baseada em qualidade | Fluxo VBR baseado em taxa de bits (restrito ou não restrito) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Para enumerar os formatos com suporte para um codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) para encontrar o número de codecs com suporte. Em seguida, [**chame IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) para cada formato. Os índices de formato variam de zero a um a menos que o número total de formatos com suporte. Você pode recuperar uma descrição do formato chamando [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Ao usar **GetCodecFormatDesc**, você não precisa usar **GetCodecFormat**, porque o objeto de configuração de fluxo é recuperado por ambos os métodos. Os formatos de codec de vídeo não incluem uma descrição. Cada codec de vídeo tem apenas um formato que é usado para todos os fluxos desse tipo.

Ao recuperar um formato codec, você obterá a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de um objeto de configuração de fluxo que contém as configurações de formato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obter informações de configuração de fluxo de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




