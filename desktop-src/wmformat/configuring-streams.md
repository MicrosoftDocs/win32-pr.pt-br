---
title: configurando Fluxos
description: configurando Fluxos
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows SDK do formato de mídia, fluxos
- perfis, fluxos
- fluxos, configurando
- codecs, configurando fluxos
- perfis, interface IWMStreamConfig
- fluxos, interface IWMStreamConfig
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199312"
---
# <a name="configuring-streams"></a>configurando Fluxos

A única coisa que é necessária em um perfil é pelo menos um fluxo. As outras opções fornecem acesso a recursos mais avançados, mas com o mínimo de um fluxo, você pode criar um arquivo ASF. É essencial que você entenda como configurar fluxos antes de criar perfis complexos.

para fins de perfis, os fluxos podem ser divididos em dois tipos: aqueles compactados com Windows codecs de mídia e fluxos arbitrários que não são processados com nenhum codec. fluxos de áudio e fluxos de vídeo são os tipos que usam os codecs de mídia Windows. É claro que os fluxos podem conter áudio ou vídeo compactados com um codec de terceiros, mas o processo de configuração desse tipo de fluxo é um caso especial. Para obter mais informações, consulte [para criar arquivos ASF usando codecs de](to-create-asf-files-using-third-party-codecs.md)terceiros.

A lista a seguir resume o processo de configuração de um fluxo.

1.  Obtenha um objeto de configuração de fluxo para o fluxo.
    -   se você estiver criando um fluxo usando um dos codecs de mídia Windows, deverá obter o objeto de configuração de fluxo como um formato de codec usando os métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3).
    -   Se o fluxo for um tipo arbitrário, obtenha um objeto de configuração de fluxo vazio usando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configure o fluxo para atender às suas necessidades.
    -   Fluxos de todos os tipos devem ser atribuídos um nome, um nome de conexão e um número de fluxo.
    -   Fluxos usando Windows codecs de mídia devem ser alterados apenas de maneiras predefinidas do formato de codec. Para fluxos de áudio, somente as configurações de taxa de bits variável (VBR) para a VBR de duas passagens devem ser alteradas. Fluxos de vídeo precisam ser configurados com as propriedades de quadro desejadas.
    -   Os fluxos arbitrários têm requisitos de configuração variados por tipo. Todos exigem uma taxa de bits e uma janela de buffer.
3.  Adicione o fluxo ao perfil chamando [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Todos os fluxos são definidos usando objetos de configuração de fluxo. A interface principal para um objeto de configuração de fluxo é [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), que fornece métodos para definir as configurações básicas de um fluxo, como o número do fluxo, a taxa de bits e assim por diante. **IWMStreamConfig** é herdado pelas interfaces mais recentes, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) e [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Assim como acontece com todas as revisões de interface numeradas, você sempre deve recuperar a versão mais recente usando o método **QueryInterface** .

A maioria das configurações em um fluxo é acessada por meio de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). Essas configurações são encapsuladas em uma estrutura de [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Para áudio e vídeo, a estrutura do **\_ \_ tipo de mídia do WM** aponta para outra estrutura com informações adicionais específicas para o tipo de mídia. Normalmente, essa estrutura secundária é [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) para áudio e [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para vídeo. Além disso, os fluxos de vídeo têm uma estrutura terciário, **BITMAPINFOHEADER**, que descreve as características de um quadro de vídeo individual. **BITMAPINFOHEADER** é uma estrutura comum e pode ser encontrada na seção Graphics Device Interface (GDI) do Platform SDK.

As seções a seguir descrevem como configurar fluxos.



| Seção                                                                                                          | Descrição                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [configuração comum a todos os Fluxos](configuration-common-to-all-streams.md)                                   | Descreve a configuração básica de fluxo comum a todos os tipos de fluxos.                                                                                        |
| [Obtendo informações de configuração de fluxo de codecs](getting-stream-configuration-information-from-codecs.md) | descreve como obter informações de configuração de fluxo dos codecs para garantir a configuração adequada de fluxos usando os codecs de áudio e vídeo de mídia Windows. |
| [configurando Fluxos de áudio](configuring-audio-streams.md)                                                       | Descreve como configurar fluxos de áudio.                                                                                                                       |
| [configurando Fluxos de vídeo](configuring-video-streams.md)                                                       | Descreve como configurar fluxos de vídeo.                                                                                                                       |
| [configurando Fluxos de vídeo para busca de desempenho](configuring-video-streams-for-seeking-performance.md)       | Descreve como configurar fluxos de vídeo para os quais uma busca eficiente é importante.                                                                              |
| [configurando a captura de tela Fluxos](configuring-screen-capture-streams.md)                                     | Descreve como configurar fluxos de vídeo para captura de tela.                                                                                                    |
| [configurando a Fluxos de imagem](configuring-image-streams.md)                                                       | Descreve como configurar fluxos de imagem.                                                                                                                       |
| [usando Fluxos de áudio e vídeo não compactados](using-uncompressed-audio-and-video-streams.md)                     | Descreve como configurar um fluxo de áudio ou vídeo não compactado.                                                                                                  |
| [Configurando tipos de fluxo arbitrários](configuring-arbitrary-stream-types.md)                                     | Descreve como configurar fluxos para usar os tipos de fluxo arbitrários predefinidos.                                                                                |
| [configurando Fluxos de VBR](configuring-vbr-streams.md)                                                           | Descreve como configurar fluxos para usar a VBR (codificação de taxa de bits) variável.                                                                                     |
| [Configurar extensões de unidade de dados](configuring-data-unit-extensions.md)                                         | Descreve como configurar um fluxo para que as extensões de unidade de dados possam ser anexadas quando o arquivo for gravado.                                                      |
| [Reutilizando configurações de fluxo](reusing-stream-configurations.md)                                               | Descreve as maneiras pelas quais você pode usar objetos de configuração de fluxo de perfis existentes para criar novos perfis.                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 