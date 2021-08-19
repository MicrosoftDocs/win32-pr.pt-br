---
description: Saiba mais sobre como criar o sink de arquivo ASF, que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Criando o sink de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ed3aeb3082277fa3a8bb4c814c1a82f92dd3da8815ffdbd70e4ef87d0d4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743254"
---
# <a name="creating-the-asf-file-sink"></a>Criando o sink de arquivo ASF

O sink de arquivo ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto e o uso geral dos sinks de mídia do ASF, consulte [AsF Media Sinks](asf-media-sinks.md).

Há duas maneiras de criar uma instância do sink de arquivo ASF. Você pode chamar [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) ou [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Se você chamar [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), deverá especificar um fluxo de byte para o arquivo de saída, no qual o sink gravará o conteúdo ASF durante uma sessão de codificação. O fluxo de byte especificado deve ter funcionalidades que podem ser buscadas e que podem ser escritas; caso contrário, a chamada **MFCreateASFMediaSink** falhará com o código de erro E \_ FAIL. Essa chamada cria um objeto de sink de arquivo em processo e retorna um ponteiro para a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do sink de arquivo.

Se você chamar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), deverá especificar a URL do arquivo de saída no qual o sink de arquivo gravará dados de mídia. Nesse caso, o sink de arquivo cria internamente o fluxo de byte. A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do sink de arquivo. Para

Considere [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) em vez de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), quando sua topologia de codificação for projetada da seguinte forma:

-   A topologia de codificação é para o caminho de mídia protegido (PMP) e o sink de arquivo é usado fora do processo.
-   O nó de saída da topologia é criado usando o ponteiro retornado para o objeto de ativação do sink de arquivo e seu aplicativo está acompanhando os fluxos no sink de arquivos por números de fluxo.
    > [!Note]  
    > Você pode ativar o sink de arquivo chamando [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). No entanto, você não precisa ativar o objeto de forma explictly. A Sessão de Mídia mantém o controle do objeto de ativação e ativa o sink de arquivo automaticamente durante a sessão de codificação.

     

-   As informações de fluxo são configuradas no objeto ContentInfo. Sem sucesso na próxima subseção.

Depois de criar o sink de arquivo ASF, ele deve ser configurado antes de criar a topologia. O sink de arquivo precisa saber as informações a seguir para gerar o arquivo de saída.

-   Informações básicas do fluxo
-   Informações do modo de codificação
-   Metadados

O sink de arquivo implementa o Objeto [ContentInfo do ASF](asf-contentinfo-object.md) e expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) para que um aplicativo possa usá-lo para definir informações relacionadas aos fluxos e codificação. Dependendo da função que você chamou para criar o sink de arquivo, há duas maneiras de obter uma referência à interface **IMFASFContentInfo.**

-   Se você chamar a [**função MFCreateASFMediaSink,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) o aplicativo deverá consultar a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chamando **IMFMediaSink::QueryInterface** no sink de arquivo retornado.
-   Se você optar por chamar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), essa função espera que você tenha um objeto ContentInfo totalmente configurado antes da chamada. Para fazer isso, você precisa criar um objeto ContentInfo vazio chamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e configurá-lo com todas as informações necessárias. Passe o objeto ContentInfo configurado para **O MFCreateASFMediaSinkActivate** para receber um ponteiro para o objeto de ativação do sink. Você não pode ativar o sink de arquivo usando o objeto de ativação retornado e, em seguida, alterar qualquer informação de fluxo ou codificação.

Para obter informações sobre como configurar fluxos de sink e propriedades específicas, consulte os seguintes tópicos:

-   [Adicionando informações de fluxo ao sink do arquivo ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Definindo propriedades no sink de arquivo](setting-properties-in-the-file-sink.md)
-   [Adicionando metadados ao sink de arquivo](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sinks de mídia do ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



