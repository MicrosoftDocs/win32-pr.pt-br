---
description: O coletor de arquivos ASF é uma implementação de IMFMediaSink fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto de coletor de mídia ASF e uso geral, consulte coletores de mídia ASF.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Definindo propriedades no coletor de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30af39cf13e88f6edf2a6ab68caac27c2400955a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296529"
---
# <a name="setting-properties-in-the-file-sink"></a>Definindo propriedades no coletor de arquivos

O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).

Depois de [criar o coletor de arquivo ASF](creating-the-asf-file-sink.md), ele deve ser configurado com informações sobre os fluxos no arquivo de saída. Esse procedimento é descrito em [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md). Você pode definir propriedades adicionais no coletor de arquivos dependendo do tipo de codificação; buckets vazados; Propriedades gerais do arquivo. Essas configurações não são gravadas no objeto de cabeçalho ASF final. Este tópico descreve o processo de adicionar essas propriedades no repositório de propriedades do coletor de arquivos.

O objeto ContentInfo mantém as propriedades de arquivo global e as propriedades de fluxo individuais para o coletor de arquivos. Para obter informações sobre como obter uma referência ao objeto ASF ContentInfo do coletor de arquivos, consulte [criando o coletor de arquivo ASF](creating-the-asf-file-sink.md).

Para obter uma referência ao repositório de propriedades do coletor de arquivos ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)), chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) na referência do objeto ContentInfo do coletor de arquivos.

## <a name="stream-encoding-properties"></a>Propriedades de codificação de fluxo

Para codificar o conteúdo corretamente, o arquivo precisa saber certas informações de codificação, como tipo de codificação e os parâmetros de codificação relacionados. Esses valores são definidos no coletor de arquivos como valores de propriedade em um repositório de propriedades que é mantido pelo objeto ContentInfo do ASF. Se você estiver configurando o coletor de arquivos antes de instanciar os codificadores relevantes, poderá usar o objeto ContentInfo com todas as propriedades preenchidas para criar os codificadores de mídia do Windows. Nesse caso, as propriedades são definidas automaticamente nos codificadores instanciados. Por outro lado, se você estiver criando os codificadores antes do coletor, certifique-se de que as propriedades definidas nos codificadores sejam copiadas no repositório de propriedades do coletor de arquivos.

Para definir as propriedades de codificação, você precisa ter acesso ao armazenamento de propriedades no nível de fluxo do coletor de arquivos. Passe o número do fluxo no parâmetro *wStreamNumber* do método [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Os números de fluxo devem corresponder aos valores definidos durante a configuração de cada fluxo no perfil. Os valores de propriedade são definidos chamando [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). A tabela a seguir descreve as propriedades com suporte.

As propriedades dependem do tipo de codificação. Para obter informações sobre as propriedades e os respectivos valores que você deve definir, consulte [Propriedades de codificação](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Propriedade de Bucket vazado

Os parâmetros de Bucket de vazamento determinam a janela de buffer real usada pelo codificador para o fluxo. A propriedade [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigida \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) do coletor de arquivos contém os parâmetros de Bucket de vazamento, a taxa de bits, a janela de buffer e a totalidade do buffer inicial. Essa propriedade é definida no repositório de propriedades de propriedade de nível de fluxo para o coletor de arquivo e deve ser definida depois que os codificadores tiverem sido criados e configurados. Esse valor é definido em. Durante a negociação do tipo de mídia, o codificador decide a janela de buffer e a taxa de bits a ser usada. Você pode obter esses valores usando a interface **IWMCodecLeakyBucket** , que é definida em wmcodecifaces. h, e você deve vincular a wmcodecdspuuid. lib para chamar seus métodos.

Os valores recuperados podem ser definidos para essa propriedade para cada fluxo no coletor de arquivo ASF.

## <a name="global-file-sink-properties"></a>Propriedades do coletor de arquivo global

Para obter o repositório de propriedades globais do coletor de arquivos, passe 0 no parâmetro *wStreamNumber* do método [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Os valores de propriedade são definidos chamando [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). A tabela a seguir descreve as propriedades com suporte.

| Propriedades de nível de arquivo                                                                                | Descrição                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Enviar MFPKEY ASFMEDIASINK \_ base \_**](mfpkey-asfmediasink-base-sendtime-property.md)           | O tempo de envio indica quando a carga dentro do Bucket de vazamento será liberada. Esse valor de propriedade indica a primeira hora de envio. O multiplexador usa esse valor para calcular os tempos de envio subsequentes para os pacotes gerados e garante que os dados fluem de forma estável por meio do Bucket vazado. |
| [**MFPKEY \_ ASFMEDIASINK \_ AutoAjuste de \_ taxa de bits**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Esse valor BOOL indica se o multiplexador precisa ajustar a taxa de bits automaticamente para garantir que os dados não estourem o Bucket de vazamentos.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Isso indica a ação de DRM do coletor de mídia do ASF para geração de arquivos. Nesta versão, somente a transcodificação DRM tem suporte.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletores de mídia ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
