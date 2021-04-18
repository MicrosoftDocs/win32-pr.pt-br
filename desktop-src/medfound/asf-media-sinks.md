---
description: O coletor de mídia ASF é o componente final no pipeline de codificação que permite que um aplicativo grave um arquivo ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Coletores de mídia ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759159"
---
# <a name="asf-media-sinks"></a>Coletores de mídia ASF

O coletor de mídia ASF é o componente final no pipeline de codificação que permite que um aplicativo grave um arquivo ASF.

Media Foundation fornece dois tipos de coletores de mídia ASF:

-   O *coletor de arquivos ASF* é usado para arquivar dados de mídia ASF em um arquivo.
-   O *coletor de streaming ASF* é usado para gravar conteúdo ASF em um fluxo de bytes que pode ser transmitido pela rede.

Os coletores de mídia ASF contêm um ou mais coletores de fluxo, que representam os dados a serem gravados para cada fluxo no arquivo ASF de saída. Para codificar aplicativos executados no Windows Vista, você deve configurar manualmente a topologia de codificação criando e Configurando o coletor de mídia ASF e, em seguida, adicionando-o à topologia. No Windows 7, se você estiver usando os objetos de transcodificação rápida para criar a topologia, você não terá criar o coletor de mídia diretamente e o aplicativo não chamará nenhum método no coletor de mídia ou qualquer um dos coletores de fluxo. Os objetos de transcodificação rápida instanciam os coletores de mídia necessários e os adicionam à topologia antes de retornar uma referência ao aplicativo chamador. No entanto, para objetos de transcodificação rápidos, há algumas restrições que se aplicam dependendo do tipo de codificação.

-   [Modelo de objeto de coletor de mídia ASF](#asf-media-sink-object-model)
-   [Coletor de arquivo ASF](#asf-file-sink)
-   [Tópicos relacionados](#related-topics)

## <a name="asf-media-sink-object-model"></a>Modelo de objeto de coletor de mídia ASF

Os coletores de mídia ASF implementam a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) e expõem as interfaces a seguir. Um aplicativo pode obter uma referência a essas interfaces chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no coletor de mídia do ASF que está usando para gerar amostras de saída.



| Interface                                                  | Descrição                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | Necessário para todos os coletores de mídia.                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | Implementado pelo coletor de arquivo ASF que grava o conteúdo de mídia gerado em um arquivo. Você pode usar os métodos nessa interface para liberar dados e atualizar o objeto de cabeçalho ASF do arquivo de saída final. |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | Recebe notificações de alteração de estado do relógio de apresentação.                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | O objeto ASF ContentInfo é um objeto de nível WMContainer que armazena principalmente informações de objeto de cabeçalho ASF. Isso é usado para criar coletores de mídia ASF.                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | Usado para descrever os metadados para o arquivo ASF.                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | Recupera uma coleção de metadados, seja para uma apresentação inteira ou para um fluxo na apresentação.                                                                                          |



 

## <a name="asf-file-sink"></a>Coletor de arquivo ASF

O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.

Você precisa criar, configurar e chamar métodos no coletor de arquivos ou qualquer um de seus coletores de fluxo se estiver usando os objetos da camada de pipeline para gravar um novo arquivo ASF. Depois de configurar o coletor de arquivos, você pode adicioná-lo ao pipeline de codificação.

Aqui estão as etapas gerais para usar o coletor de arquivo ASF:

1.  Crie o coletor de arquivos em processo ou fora de processo.
2.  Configure o coletor de arquivos com todos os fluxos, propriedades de codificação e informações de metadados.
3.  Associe o coletor de arquivos ao nó de topologia de saída enumerando os coletores de fluxo ou controlando os números de fluxo com no coletor.

Os tópicos a seguir contêm informações detalhadas sobre como trabalhar com o coletor de arquivos ASF:

-   [Criando o coletor de arquivo ASF](creating-the-asf-file-sink.md)
-   [Adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md)
-   [Definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md)
-   [Adicionando metadados ao coletor de arquivos](adding-metadata-to-the-file-sink.md)
-   [O modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
