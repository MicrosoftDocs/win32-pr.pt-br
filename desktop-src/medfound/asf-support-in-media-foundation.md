---
description: Suporte a ASF no Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Suporte a ASF no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784614"
---
# <a name="asf-support-in-media-foundation"></a>Suporte a ASF no Media Foundation

O Media Foundation dá suporte a arquivos de mídia no ASF (Advanced Systems Format):

-   Vídeo do Windows Media (arquivos WMV)
-   Áudio do Windows Media (arquivos WMA)

O Media Foundation fornece vários objetos para ler e gravar arquivos ASF. Esses objetos são fornecidos em duas camadas de arquitetura diferentes.

Primeiro, a camada de *pipeline* contém objetos que funcionam dentro do [pipeline de Media Foundation](media-foundation-pipeline.md) e estão em conformidade com as APIs definidas pelo pipeline. A camada de pipeline do ASF contém:

-   [Fonte de mídia ASF](asf-media-source.md): analisa arquivos ASF e entrega os pacotes de dados de áudio/vídeo.
-   [Codecs de mídia do Windows](windows-media-codecs.md): decodificar ou codificar fluxos de áudio ou vídeo do Windows Media.
-   [Coletor de mídia ASF](asf-media-sinks.md): recebe pacotes de dados e grava um arquivo asf.

Em segundo lugar, a camada de contêiner do WM fornece controle de baixo nível sobre a análise e a gravação de um arquivo ASF. A camada de pipeline usa WMContainer internamente. Os aplicativos também podem usar WMContainer para análise e gravação de ASF de baixo nível.

![diagrama mostrando elementos da camada de pipeline e do contêiner do WM](images/asf-components.png)

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                         | Descrição                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Estrutura de arquivo ASF](asf-file-structure.md)<br/>                       | Visão geral da estrutura do arquivo ASF e dos objetos fornecidos pelo Media Foundation para trabalhar com arquivos ASF.<br/> |
| [Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)<br/> | Descreve como analisar e criar arquivos ASF usando a camada de pipeline.<br/>                                   |
| [Componentes ASF WMContainer](wmcontainer-asf-components.md)<br/>       | Descreve como analisar e criar arquivos ASF usando a camada WMContainer.<br/>                                |



 

Para obter informações detalhadas sobre a estrutura de um arquivo ASF, consulte a especificação do ASF, que pode ser baixada deste [site da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




