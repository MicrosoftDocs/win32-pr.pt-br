---
description: Configurando o objeto divisor ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configurando o objeto divisor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7068f2c869f6c73447b3341baee7221cdf8efbacec47ecdfa3a584bfb456f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606146"
---
# <a name="configuring-the-asf-splitter-object"></a>Configurando o objeto divisor ASF

O objeto *divisor* ASF é um objeto de camada WMContainer que analisado o objeto de dados ASF de um arquivo ASF (Advanced Systems Format). Depois que o divisor é criado e inicializado para analisar o Objeto de Dados ASF de um arquivo de mídia, o divisor deve ser configurado para gerar exemplos para fluxos específicos. Chame [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para selecionar os fluxos necessários.

Opcionalmente, um aplicativo também pode configurá-lo para gerar exemplos em ordem inversa ou gerar exemplos de conteúdo protegido. Para definir essas opções, chame [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) e passe a combinação bit a bit necessária dos sinalizadores com suporte. Antes de chamar esse método, o cliente deve concluir a [**chamada IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) com êxito; caso contrário, **SetFlags falhará** com o código **de erro MF \_ E NOT \_ \_ INITIALIZED.** Para obter informações sobre como inicializar o divisor, consulte [Criando o objeto divisor ASF](creating-the-asf-splitter-object.md).

Para verificar se esse sinalizador está atualmente definido no divisor, chame [**IMFASFSplitter::GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Selecionando Fluxos para análise

Durante o processo de inicialização por meio da chamada [**IMFASFSplitter::Initialize,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) o divisor detecta o número de fluxos e os identificadores de fluxo no arquivo ASF. Por padrão, nenhum fluxo é selecionado pelo divisor. O aplicativo deve selecionar os fluxos chamando [**IMFASFSplitter::SelectStreams.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) Esse método aceita uma matriz de números de fluxo. Para obter o número de fluxo de um fluxo, chame [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) no perfil do ASF ou chame [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) no descritor de fluxo. (Você pode obter o perfil ASF e o descritor de fluxo do objeto ContentInfo.) Se o cliente passar um número de fluxo que não é reconhecido pelo divisor, ele falhará com um erro **MF \_ E \_ INVALIDSTREAMNUMBER.**

Chamar [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) limpa as seleções anteriores. Qualquer fluxo que não seja especificado na matriz não está selecionado. Para obter uma lista de fluxos selecionados no momento, chame [**IMFASFSplitter::GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Esse método leva um ponteiro para uma matriz, que o método preenche com os números de fluxo. Se o tamanho da matriz for menor que o número de fluxos selecionados, o método falhará com o **erro MF \_ E \_ BUFFERTOOSMALL.** Nesse caso, o método retorna o número de fluxos selecionados no *parâmetro pwNumStreams.* Em seguida, você pode usar esse número para alocar uma matriz do tamanho correto e chamar o método novamente.

Por exemplo, consulte "Selecionar um fluxo para análise" no [Tutorial: Lendo um arquivo ASF](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Configuração de reprodução inversa

Durante o processo de inicialização do divisor, ele determina se o conteúdo do ASF dá suporte à reprodução inversa. Se isso acontecer, o divisor poderá ser configurado para gerar exemplos em ordem inversa definindo o sinalizador **\_ REVERSE SPLITTER \_ DE MFASF.** Se o conteúdo não dá suporte à reprodução inversa, [**o IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) retorna **MF \_ E \_ INVALIDREQUEST,** mas o sinalizador é definido no divisor.

Se o divisor estiver configurado para analisar na direção inversa, o divisor sempre iniciará a análise no final do buffer que contém o Objeto de Dados ASF. Portanto, para a análise inversa do deslocamento de dados e o comprimento dos dados a serem analisados devem ser definidos adequadamente. Para obter informações sobre como definir os valores [corretos, consulte Gerando exemplos de fluxo de um objeto de dados ASF existente.](generating-stream-samples-from-an-existing-asf-data-object.md)

## <a name="protected-content-setting"></a>Configuração de conteúdo protegido

O divisor pode ser configurado para funcionar com o conteúdo de criptografia no nível do pacote definindo o **\_ \_ WMDRM SPLITTER MFASF** por [**meio de IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). Isso instrui o divisor a fornecer exemplos de conteúdo protegido pelo DRM (Windows Media Digital Rights Management). Quando esse sinalizador é definido, os exemplos gerados pelo divisor contêm informações necessárias para descriptografar dados de mídia e reconstruir os quadros, como o atributo [**MFSampleExtension \_ PacketCrossOffsets.**](mfsampleextension-packetcrossoffsets-attribute.md) Esse atributo é um blob que contém uma matriz **de DWORD** s. Cada **DWORD** fornece os limites de carga para o quadro em relação ao início do quadro. Se esse atributo não estiver presente, o quadro estará contido em uma única carga. Normalmente, os exemplos gerados pelo divisor contêm vários buffers de mídia, o aplicativo pode copiar todos os buffers em um buffer contíguo chamando [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). O buffer resultante contém o quadro e o valor do atributo contém deslocamentos para esse buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Divisor ASF](asf-splitter.md)
</dt> </dl>

 

 



