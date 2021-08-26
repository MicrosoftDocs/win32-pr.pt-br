---
title: Visão geral do formato ASF
description: Visão geral do formato ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows SDK do formato de mídia, visão geral do formato ASF
- Formato de sistema avançado (ASF), visão geral de formato
- ASF (formato de sistemas avançados), visão geral de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee075330e9c68ef1fbdadea12c70fd8deec584f99f8dadd31cb55070dc11eee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930556"
---
# <a name="overview-of-the-asf-format"></a>Visão geral do formato ASF

O ASF (Advanced Systems Format) é um formato de arquivo extensível projetado principalmente para armazenar e reproduzir fluxos de mídia digital sincronizados e transmiti-los por redes. ASF é o formato de contêiner para Windows mídia de áudio e Windows conteúdo baseado em vídeo de mídia. a extensão wma ou wmv é usada para especificar um arquivo ASF que contém o conteúdo codificado com os codecs de vídeo Windows mídia e/ou Windows media. o SDK do formato de mídia Windows pode ser usado para criar e ler Windows arquivos de mídia, bem como arquivos ASF que contêm outros tipos de dados compactados ou descompactados.

Esta seção fornece uma descrição geral do formato ASF como informações de segundo plano. Como os objetos Reader e Writer lidam com todas as tarefas de formatação e análise de arquivo de nível baixo, não é necessário ter uma compreensão detalhada do ASF antes de usar esse SDK para criar arquivos ASF. A especificação ASF completa pode ser encontrada no [site da Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Os principais objetivos do formato ASF são:

-   Para dar suporte à reprodução eficiente de servidores de mídia, servidores HTTP e dispositivos de armazenamento local.
-   Para dar suporte a tipos de mídia escalonáveis, como áudio e vídeo.
-   Para permitir que uma única composição de multimídia seja apresentada em uma ampla gama de larguras de banda.
-   Para permitir o controle de criação sobre relações de fluxo de mídia, especialmente em cenários de largura de banda restrita.
-   Para ser independente de qualquer sistema de composição de multimídia, sistema operacional de computador ou protocolo de comunicação de dados específico.

Um arquivo ASF pode conter vários fluxos independentes ou dependentes, incluindo vários fluxos de áudio para áudio de vários canais ou fluxos de vídeo de taxa de bits múltiplos adequados para transmissão por diferentes larguras de banda. Os fluxos podem estar em qualquer formato compactado ou descompactado; no entanto, a melhor compactação é obtida com os codecs de áudio Microsoft Windows Media e vídeo 9 Series. Além dos tipos de fluxo de mídia de vídeo e áudio padrão, um arquivo ASF também pode conter fluxos de texto, páginas da Web e comandos de script e qualquer outro tipo de dados arbitrário. O ASF dá suporte a conteúdo de multimídia ao vivo e sob demanda. Ele pode ser usado como um veículo para gravar ou reproduzir o H. 32X (por exemplo, H. 323 e H. 324) ou MBONE conferências.

Um arquivo ASF é organizado em seções chamadas "objetos". Há três objetos de nível superior, um objeto de cabeçalho e um objeto de dados (ambos necessários), além de um objeto de índice opcional. O objeto de cabeçalho contém informações gerais sobre o arquivo, como o tamanho do arquivo, o número de fluxos, os métodos de correção de erro e os codecs usados. Os metadados também são armazenados aqui. O objeto de cabeçalho é o único objeto de nível superior que pode conter outros objetos. O objeto de dados contém os dados de fluxo, organizados em pacotes. O objeto de índice simples contém uma lista de pares de índice/chave-quadro associados que permite que os aplicativos procurem um arquivo com eficiência. O índice associado a cada quadro-chave pode ser uma hora de apresentação, um número de quadro de vídeo ou um carimbo de data/hora de referência.

Cada objeto de nível superior ou de nível inferior começa com um GUID (identificador global exclusivo) e um valor de tamanho. Esses números permitem que o leitor de arquivos analise as informações em locais apropriados em objetos identificáveis. Devido a esses GUIDs, os objetos de nível inferior podem ser enviados em qualquer ordem e ainda serem reconhecidos. O formato ASF foi projetado para superar a recepção de dados imprecisa. Um arquivo ASF parcialmente baixado ainda pode ser lido, contanto que ele contenha o objeto de cabeçalho e pelo menos um objeto de dados.

Informações detalhadas sobre o ASF no apresentado na especificação do ASF. Você pode baixar a especificação no [site da Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre o SDK do formato de mídia Windows**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




