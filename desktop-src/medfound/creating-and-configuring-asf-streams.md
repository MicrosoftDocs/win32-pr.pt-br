---
description: Cada arquivo ASF contém um ou mais fluxos. O objeto de perfil ASF representa uma coleção de fluxos ASF. Para a codificação ASF, você deve criar e configurar os fluxos que deseja codificar.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: criando e configurando Fluxos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c780de3fa0abb5db29e3e5e5ed049b78aca7898966e8f7e8595b504804da91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743234"
---
# <a name="creating-and-configuring-asf-streams"></a>criando e configurando Fluxos ASF

Cada arquivo ASF contém um ou mais fluxos. O objeto de [perfil ASF](asf-profile.md) representa uma coleção de fluxos ASF. Para a codificação ASF, você deve criar e configurar os fluxos que deseja codificar.

Um aplicativo pode executar as seguintes tarefas com o objeto de perfil ASF:

-   Adicionar ou remover um fluxo.
-   Obter as definições de configuração de um fluxo.
-   Configurar extensões de carga.
-   Adicionar, remover ou modificar um objeto de exclusão mútua ASF.

Este tópico inclui as seções a seguir.

-   [Criando um novo fluxo](#creating-a-new-stream)
-   [Atribuindo números de fluxo](#assigning-stream-numbers)
-   [Definindo valores de buckets vazados](#setting-leaky-bucket-values)
-   [Extensões de carga](#payload-extensions)
-   [Adicionando um fluxo ao perfil](#adding-a-stream-to-the-profile)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-new-stream"></a>Criando um novo fluxo

Um objeto de perfil ASF deve conter definições de configuração para pelo menos um fluxo ASF. Cada fluxo é representado por um objeto de *configuração de fluxo* , que expõe a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . As informações no objeto de configuração de fluxo correspondem ao objeto de propriedades de fluxo e aos objetos de propriedades de fluxo estendidos no cabeçalho do arquivo ASF. (Consulte a [estrutura do arquivo ASF](asf-file-structure.md).)

Para adicionar um fluxo a um perfil ASF, execute as seguintes etapas:

1.  Crie um objeto de configuração de fluxo de fluxo vazio.
2.  Configure o fluxo de acordo com os requisitos do aplicativo.
3.  Adicione o fluxo ao perfil.

Para criar um fluxo para o perfil, chame [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para criar um objeto de configuração de fluxo vazio e receber o ponteiro no parâmetro *ppIStream* . **CreateStream** precisa saber o tipo do fluxo a ser criado. Os tipos mais comuns de fluxos usados em arquivos ASF são fluxos de áudio e vídeo. No Media Foundation, os tipos de fluxo são indicados pelo objeto de tipo de mídia que expõe a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . O tipo principal do tipo de mídia define a categoria do fluxo de mídia digital, como áudio ou vídeo. O subtipo define o formato do tipo principal. O tipo de mídia inicial definido por **CreateStream** pode ser alterado usando o objeto de configuração de fluxo. Para recuperar o tipo de mídia para o fluxo, chame [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) ou recupere a chamada de tipo principal [**IMFASFStreamConfig:: getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). O tipo de mídia inicial para um fluxo pode ser substituído por um novo tipo de mídia configurado chamando [**IMFASFStreamConfig:: SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Se um aplicativo criar um perfil de um descritor de apresentação válido chamando [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). A função define automaticamente os objetos de configuração de fluxo para cada um dos fluxos e os define no perfil. Os tipos de mídia de fluxo são definidos com base nos descritores de fluxo associados ao descriptor de apresentação.

## <a name="assigning-stream-numbers"></a>Atribuindo números de fluxo

um número de fluxo Fluxos de todos os tipos deve ser atribuído. Os números de fluxo não precisam ser sequenciais, mas devem estar no intervalo de 1 a 127. Para atribuir números de fluxo, chame [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Para obter a chamada de número de fluxo, [**IMFASFStreamConfig:: GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Um número de fluxo é diferente de um índice de fluxo, que você usa ao obter fluxos em um perfil usando [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream). O índice de fluxo é um número atribuído ao fluxo pelo objeto de perfil. Os índices de fluxo variam entre 0 e um menor que o número de fluxos recuperados por [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). Você também pode obter um fluxo do perfil por número de fluxo chamando [**IMFASFProfile:: GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Definindo valores de buckets vazados

Cada objeto de configuração de fluxo que representa um fluxo deve ter parâmetros de Bucket de vazamento associados, taxa de bits e valores de janela de buffer.

Esses valores estão disponíveis para o aplicativo por meio do atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e o atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) . Para codificação de arquivo, os valores reais dependem do tipo de codificação e são decididos pelo codificador. Se você já tiver um codificador configurado e o tipo de saída estiver definido no codificador, o aplicativo deverá consultar o codificador quanto aos parâmetros de Bucket de vazamento e definir os valores nesses atributos.

Se você estiver usando os componentes da camada de pipeline e configurando os fluxos para o coletor de mídia ASF, provavelmente não terá um codificador configurado. Nesse caso, você deve consultar as negociações do tipo post-Media do codificador e definir o valor atualizado na propriedade [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK corrigida do MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) do repositório de propriedades do coletor de mídia do ASF. O armazenamento de propriedade de codificação é recuperado por meio do do objeto ContentInfo associado ao perfil. Os valores atualizados são refletidos automaticamente nos valores de atributo de Bucket vazado do fluxo. Para obter informações gerais sobre buckets vazados e como obter o valor de Bucket de vazamento do codificador, consulte o [modelo de buffer de buckets de vazamentos](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Extensões de carga

Os dados de mídia para os fluxos são adicionados ao objeto de dados ASF como [amostras de mídia](media-samples.md) pelo [Multiplexador de ASF](asf-multiplexer.md). Esses exemplos de mídia podem conter dados de extensão de carga: dados de código de tempo SMPTE, taxa de proporção de pixel não quadrado, duração de amostra e, se o exemplo contiver, um quadro de chave de vídeo. Para obter uma lista dos tipos de extensão de carga com suporte, consulte [GUIDs de extensão de carga ASF](asf-payload-extension-guids.md).

Um fluxo deve ser configurado para aceitar a extensão de carga para que durante a geração de amostra o multiplexador possa adicionar os dados suplementares a cada amostra desse fluxo.

Para obter o número total de extensões de carga definidas no fluxo, chame [**IMFASFStreamConfig:: GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) e, em seguida, enumere a lista chamando [**IMFASFStreamConfig:: GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Para adicionar a extensão de carga para o fluxo, chame [**IMFASFStreamConfig:: AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Isso adicionará dados suplementares a amostras de mídia individuais geradas para o fluxo.

Para remover extensões de carga existentes associadas ao fluxo, chame [**IMFASFStreamConfig:: RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Adicionando um fluxo ao perfil

Depois que um fluxo é configurado, chame [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para adicionar o fluxo ao perfil.

Para remover um fluxo existente no perfil, chame [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

O perfil configurado deve ser definido no objeto ContentInfo chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Se fizer alterações em um fluxo existente, você deverá adicioná-lo novamente ao perfil e definir o perfil no objeto ContentInfo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



