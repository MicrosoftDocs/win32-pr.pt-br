---
description: Configurando o objeto divisor de ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configurando o objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f27885e602dd52012808d330d997f9b7a7e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089775"
---
# <a name="configuring-the-asf-splitter-object"></a>Configurando o objeto divisor de ASF

O objeto *divisor* de ASF é um objeto de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format). Depois que o separador é criado e inicializado para analisar o objeto de dados ASF de um arquivo de mídia, o divisor deve ser configurado para gerar amostras para fluxos específicos. Chame [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para selecionar os fluxos necessários.

Opcionalmente, um aplicativo também pode configurá-lo para gerar amostras em ordem inversa ou gerar amostras para conteúdo protegido. Para definir essas opções, chame [**IMFASFSplitter:: Setsinalizas**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) e passe a combinação de bits necessária dos sinalizadores com suporte. Antes de chamar esse método, o cliente deve concluir a chamada [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) com êxito; caso contrário, **SetFlags** falhará com o código de erro **MF \_ E \_ não \_ inicializado** . Para obter informações sobre como inicializar o divisor, consulte [criando o objeto divisor de ASF](creating-the-asf-splitter-object.md).

Para verificar se esse sinalizador está definido atualmente no divisor, chame [**IMFASFSplitter:: GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Selecionando fluxos para análise

Durante o processo de inicialização por meio de chamada [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) , o divisor detecta o número de fluxos e os identificadores de fluxo no arquivo asf. Por padrão, nenhum fluxo é selecionado pelo divisor. O aplicativo deve selecionar os fluxos chamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams). Esse método usa uma matriz de números de fluxo. Para obter o número de fluxo para um fluxo, chame [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) no perfil ASF ou chame [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) no descritor de fluxo. (Você pode obter o perfil ASF e o descritor de fluxo do objeto ContentInfo.) Se o cliente passar um número de fluxo que não seja reconhecido pelo divisor, ele falhará com um erro de **MF \_ E \_ INVALIDSTREAMNUMBER** .

Chamar [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) apaga as seleções anteriores. Qualquer fluxo não especificado na matriz não é selecionado. Para obter uma lista de fluxos que estão selecionados atualmente, chame [**IMFASFSplitter:: GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Esse método usa um ponteiro para uma matriz, que o método preenche com os números de fluxo. Se o tamanho da matriz for menor que o número de fluxos selecionados, o método falhará com o erro de **MF \_ E \_ BUFFERTOOSMALL** . Nesse caso, o método retorna o número de fluxos selecionados no parâmetro *pwNumStreams* . Você pode usar esse número para alocar uma matriz do tamanho correto e chamar o método novamente.

Para obter um exemplo de código, consulte "selecionar um fluxo para análise" em [tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Configuração de reprodução reversa

Durante o processo de inicialização do divisor, ele determina se o conteúdo do ASF dá suporte à reprodução reversa. Se tiver, o separador poderá ser configurado para gerar amostras em ordem inversa, definindo o **sinalizador \_ \_ inverso do divisor MFASF** . Se o conteúdo não oferecer suporte à reprodução inversa, os [**sinalizadores IMFASFSplitter::**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) setretornarão **MF \_ E \_ INVALIDREQUEST**, mas o sinalizador será definido no separador.

Se o divisor estiver configurado para analisar na direção inversa, o divisor sempre iniciará a análise no final do buffer que contém o objeto de dados ASF. Portanto, para a análise reversa do deslocamento de dados e o comprimento dos dados a serem analisados deve ser definido adequadamente. Para obter informações sobre como definir os valores corretos, consulte [gerando amostras de fluxo de um objeto de dados ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).

## <a name="protected-content-setting"></a>Configuração de conteúdo protegido

O separador pode ser configurado para trabalhar com conteúdo de criptografia no nível de pacote definindo o **MFASF \_ Splitter \_ WMDRM** por meio de [**IMFASFSplitter:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). Isso instrui o divisor a fornecer exemplos de conteúdo protegido pelo Windows Media Digital Rights Management (DRM). Quando esse sinalizador é definido, os exemplos gerados pelo divisor contêm informações necessárias para descriptografar dados de mídia e reconstruir os quadros, como o atributo [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md) . Esse atributo é um blob que contém uma matriz de **DWORD** s. Cada **DWORD** fornece os limites de carga para o quadro em relação ao início do quadro. Se esse atributo não estiver presente, o quadro estará contido em uma única carga. Normalmente, os exemplos gerados pelo divisor contêm vários buffers de mídia, o aplicativo pode copiar todos os buffers em um buffer contíguo chamando [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). O buffer resultante contém o quadro e o valor do atributo contém deslocamentos nesse buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> </dl>

 

 



