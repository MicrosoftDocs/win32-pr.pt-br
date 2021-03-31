---
description: O coletor de arquivos ASF é uma implementação de IMFMediaSink fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto de coletor de mídia ASF e uso geral, consulte coletores de mídia ASF.
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: Criando o coletor de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43625bcbc581b4967d4db99cef71a0fc779f070
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089768"
---
# <a name="creating-the-asf-file-sink"></a>Criando o coletor de arquivo ASF

O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).

Há duas maneiras de criar uma instância do coletor de arquivos ASF. Você pode chamar [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) ou [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).

Se você chamar [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), deverá especificar um fluxo de bytes para o arquivo de saída, no qual o coletor gravará o conteúdo do ASF durante uma sessão de codificação. O fluxo de bytes especificado deve ter recursos pesquisáveis e graváveis, caso contrário, a chamada **MFCreateASFMediaSink** falhará com o \_ código de erro E falha. Essa chamada cria um objeto de coletor de arquivo em processo e retorna um ponteiro para a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do coletor de arquivos.

Se você chamar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), deverá especificar a URL do arquivo de saída no qual o coletor de arquivos gravará os dados de mídia. Nesse caso, o coletor de arquivos cria internamente o fluxo de bytes. A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do coletor de arquivos. Para

Considere [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) em vez de [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), quando sua topologia de codificação for projetada da seguinte maneira:

-   A topologia de codificação é para o caminho de mídia protegida (PMP) e o coletor de arquivos é usado fora do processo.
-   O nó de saída da topologia é criado usando o ponteiro retornado para o objeto Activate do coletor de arquivos e seu aplicativo está controlando os fluxos no coletor de arquivos por números de fluxo.
    > [!Note]  
    > Você pode ativar o coletor de arquivos chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). No entanto, não é necessário ativar o objeto explicitamente. A sessão de mídia controla o objeto de ativação e ativa o coletor de arquivos automaticamente durante a sessão de codificação.

     

-   As informações de fluxo são configuradas no objeto ContentInfo. Disucssed na próxima subseção.

Depois de criar o coletor de arquivos ASF, ele deve ser configurado antes da criação da topologia. O coletor de arquivos precisa saber as informações a seguir para gerar o arquivo de saída.

-   Informações básicas de fluxo
-   Informações do modo de codificação
-   Metadados

O coletor de arquivo implementa o [objeto ContentInfo do ASF](asf-contentinfo-object.md) e expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) para que um aplicativo possa usá-lo para definir informações relacionadas aos fluxos e à codificação. Dependendo da função que você chamou para criar o coletor de arquivos, há duas maneiras de obter uma referência à interface **IMFASFContentInfo** .

-   Se você chamar a função [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) , o aplicativo deverá consultar a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chamando **IMFMediaSink:: QueryInterface** no coletor de arquivo retornado.
-   Se você optar por chamar [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), essa função espera que você tenha um objeto ContentInfo totalmente configurado antes da chamada. Para fazer isso, você precisa criar um objeto ContentInfo vazio chamando [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) e, em seguida, configurá-lo com todas as informações necessárias. Passe o objeto ContentInfo configurado para o **MFCreateASFMediaSinkActivate** para receber um ponteiro para o objeto ativar coletor. Você não pode ativar o coletor de arquivos usando o objeto de ativação retornado e, em seguida, alterar qualquer fluxo ou informações de codificação.

Para obter informações sobre como configurar fluxos de coletor e propriedades específicas, consulte os seguintes tópicos:

-   [Adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md)
-   [Adicionando metadados ao coletor de arquivos](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletores de mídia ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



