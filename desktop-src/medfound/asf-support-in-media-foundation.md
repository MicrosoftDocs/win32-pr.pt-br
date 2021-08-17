---
description: Suporte a ASF em Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Suporte a ASF em Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db06c5a294e351b09d7f5327e8ee22891798671765bc5cc10eafd75785debde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880949"
---
# <a name="asf-support-in-media-foundation"></a>Suporte a ASF em Media Foundation

Media Foundation dá suporte a arquivos de mídia no ASF (Advanced Systems Format):

-   Windows Vídeo de mídia (arquivos WMV)
-   Windows Áudio de mídia (arquivos WMA)

Media Foundation fornece vários objetos para ler e escrever arquivos ASF. Esses objetos são fornecidos em duas camadas de arquitetura diferentes.

Primeiro, a *camada de pipeline* contém objetos que funcionam dentro do pipeline Media Foundation [e](media-foundation-pipeline.md) estão em conformidade com as APIs definidas pelo pipeline. A camada de pipeline do ASF contém:

-   [Fonte de Mídia do ASF:](asf-media-source.md)analisar arquivos ASF e entregar os pacotes de dados de áudio/vídeo.
-   [Windows codecs de mídia:](windows-media-codecs.md)decodificar ou codificar Windows de áudio ou vídeo de mídia.
-   [AsF Media Sink:](asf-media-sinks.md)recebe pacotes de dados e grava um arquivo ASF.

Em segundo lugar, a camada contêiner WM fornece controle de baixo nível sobre a análise e a escrita de um arquivo ASF. A camada de pipeline usa WMContainer internamente. Os aplicativos também podem usar WMContainer para análise e escrita do ASF de baixo nível.

![diagrama mostrando elementos da camada de pipeline e do contêiner wm](images/asf-components.png)

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                         | Descrição                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Estrutura do arquivo ASF](asf-file-structure.md)<br/>                       | Visão geral da estrutura do arquivo ASF e dos objetos fornecidos pelo Media Foundation para trabalhar com arquivos ASF.<br/> |
| [Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)<br/> | Descreve como analisar e autor de arquivos ASF usando a camada de pipeline.<br/>                                   |
| [Componentes DOF WMContainer](wmcontainer-asf-components.md)<br/>       | Descreve como analisar e autor de arquivos ASF usando a camada WMContainer.<br/>                                |



 

Para obter informações detalhadas sobre a estrutura de um arquivo ASF, consulte a especificação do ASF, que pode ser baixada neste [site da Microsoft.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




