---
description: Ao criar um arquivo ASF, o objeto ContentInfo precisa saber as características do conteúdo de mídia para que os vários objetos de cabeçalho sejam preenchidos com os valores corretos.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Definindo propriedades no objeto ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091033"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Definindo propriedades no objeto ContentInfo

Ao criar um arquivo ASF, o objeto ContentInfo precisa saber as características do conteúdo de mídia para que os vários objetos de cabeçalho sejam preenchidos com os valores corretos.

-   [Configurações relacionadas ao conteúdo no objeto ContentInfo](#content-related-settings-in-the-contentinfo-object)
-   [Configurando o objeto ContentInfo com as configurações do codificador](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Configurações relacionadas ao conteúdo no objeto ContentInfo

As definições de configuração de conteúdo são configurações de fluxo, que estão contidas no perfil e especificam o identificador de fluxo, o tipo de mídia e os parâmetros de Bucket de vazamento para o coletor de mídia. Depois que o perfil é definido no objeto ContentInfo chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile), esses valores são refletidos no objeto de cabeçalho ASF gerado. Para obter informações sobre essas configurações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>Configurando o objeto ContentInfo com as configurações do codificador

Os dados de áudio ou vídeo de mídia digital são complexos e ocupam grandes quantidades de memória. Na maioria das circunstâncias, áudio e vídeo são compactados usando codificadores antes de serem adicionados a um arquivo ASF. Em Media Foundation, os codificadores são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFTs) com uma entrada e uma saída. Você deve selecionar o tipo de mídia de saída dependendo do tipo de mídia do fluxo de entrada e do tipo de codificação escolhido para compactar o fluxo.

Antes da sessão de codificação, o codificador deve ser configurado definindo as propriedades relevantes dependendo do tipo de codificação.

Depois de configurar o codificador, você deve configurar o objeto ContentInfo com os valores do codificador porque o [Multiplexador de ASF](asf-multiplexer.md) e o coletor de mídia ASF, que são inicializados com o objeto ContentInfo populado, usam configurações como os valores de Bucket de vazamento para gerar pacotes de dados ASF. Os valores não são salvos no objeto de cabeçalho ASF final. As configurações de codificação são expostas como propriedades. Para configurar o objeto ContentInfo com as propriedades do codificador, faça o seguinte:

1.  Obtenha um ponteiro para o repositório de propriedades do codificador consultando o codificador (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) diretamente para a interface **IPropertyStore** .
2.  Chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Para definir propriedades específicas de fluxo, especifique o identificador de fluxo no parâmetro *wStreamNumber* ; para propriedades em nível de arquivo, passe 0. O parâmetro *ppIStore* recebe um ponteiro para a interface **IPropertyStore** . O repositório de propriedades recebido está vazio.
3.  Chame **IPropertyStore:: GetValue** no codificador e obtenha o valor da propriedade especificando as constantes da chave de propriedade. Para obter uma lista completa das propriedades de codificação, consulte a [referência de programação do codec](/previous-versions//aa384554(v=vs.85)).
4.  Chame **IPropertyStore:: SetValue** no objeto ContentInfo para definir a propriedade Required no repositório de propriedades.
5.  Repita as etapas 3 e 4 para cada propriedade que você deseja definir.

O coletor de mídia do ASF pode ser criado usando um objeto de ativação chamando [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate). O novo objeto de coletor de mídia é configurado com base nas configurações específicas do coletor de mídia que podem ser definidas no repositório de propriedades do objeto ContentInfo. A tabela a seguir mostra as constantes da propriedade de coletor de mídia do ASF.



| Propriedade                                                                                                     | Descrição                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Enviar MFPKEY ASFMEDIASINK \_ base \_**](mfpkey-asfmediasink-base-sendtime-property.md)                   | O tempo de envio indica quando a carga dentro do Bucket de vazamento será liberada. Esse valor de propriedade indica a primeira hora de envio. O multiplexador usa esse valor para calcular os tempos de envio subsequentes para os pacotes gerados e garante que os dados fluem de forma estável por meio do Bucket vazado. |
| [**MFPKEY \_ ASFMEDIASINK \_ AutoAjuste de \_ taxa de bits**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Esse valor **bool** indica se o multiplexador precisa ajustar a taxa de bits automaticamente para garantir que os dados não estourem o Bucket de vazamentos.                                                                                                                                              |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                            | Isso indica a ação de DRM do coletor de mídia do ASF para geração de arquivos. Nesta versão, somente a transcodificação DRM tem suporte.                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK \_ corrigiu \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Essa propriedade deve ser definida quando o codificador decidir qual janela de buffer e taxa de bits usar. Para definir esses valores, use a interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) . Isso deve ser definido para cada fluxo no arquivo ASF.                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando um objeto de cabeçalho ASF para um novo arquivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
