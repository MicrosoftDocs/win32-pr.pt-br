---
description: Exemplo de ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Exemplo de ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db441be45d28899bc8f2ace68b8f09af40e679449d26aec7adf25ab4fb9e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959546"
---
# <a name="asfparser-sample"></a>Exemplo de ASFParser

Mostra como analisar dados de um arquivo ASF (Advanced Systems Format) usando os componentes ASF de baixo nível no Media Foundation. O exemplo demonstra as seguintes tarefas:

-   Enumerando os fluxos de áudio e vídeo em um arquivo ASF.
-   Selecionando um fluxo de áudio ou de vídeo para análise.
-   Procurando um pacote em um tempo de reprodução desejado.
-   Gerando amostras compactadas para o fluxo selecionado.
-   Decodificando amostras de áudio e vídeo.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Uso

1.  Para abrir um arquivo ASF, clique no botão **Abrir arquivo de mídia...** .
2.  Selecione um arquivo ASF e clique em **abrir**. As informações sobre o arquivo são mostradas no painel de **informações** .
3.  Em **configuração do analisador**, selecione um fluxo para analisar.
4.  Para gerar amostras em ordem inversa, selecione **Reverse**.
5.  Para especificar o ponto de partida, arraste o controle deslizante para o local desejado.
6.  Para iniciar a análise, clique no botão **gerar amostras** . As informações sobre os exemplos são mostradas no painel de **informações** .
7.  Para testar os exemplos do fluxo de áudio, clique no botão **testar áudio** .
8.  Para testar os exemplos do fluxo de vídeo, clique no botão **Mostrar bitmap** .

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

este exemplo está disponível no [repositório github de amostras clássicas do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



