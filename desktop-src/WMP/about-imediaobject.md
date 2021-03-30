---
title: Sobre o IMediaObject
description: Sobre o IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de processamento de sinal digital, interface IMediaObject
- Plug-ins do DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635084"
---
# <a name="about-imediaobject"></a>Sobre o IMediaObject

A interface **IMediaObject** é a interface necessária para o DMOs. **IMediaObject** contém os métodos que um plug-in de DSP do Windows Media Player usa para obter dados do Windows Media Player, para processar os dados e para retornar os dados processados para o Windows Media Player. Para obter a documentação completa da interface **IMediaObject** , consulte a seção DirectShow do SDK do Windows.

Os métodos de **IMediaObject** podem ser categorizados da seguinte maneira:

## <a name="methods-that-handle-format-negotiation"></a>Métodos que manipulam a negociação de formato

Esses são os métodos que o Windows Media Player chama para obter informações sobre os formatos de dados com suporte no plug-in. Esses métodos incluem:

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **Setoutputtypetype**

Vários desses métodos, como **GetInputType** e **SetInputType**, usam a estrutura do **\_ \_ tipo de mídia DMO** para descrever o formato dos dados usados por um fluxo. Quando o Windows Media Player chama esses métodos, ele fornece um ponteiro para uma estrutura de **\_ \_ tipo de mídia DMO** . Se um método como **SetInputType** especificar as informações do tipo de mídia, o plug-in deverá copiar a estrutura do **\_ \_ tipo de mídia DMO** para uma variável de membro e inspecionar seus membros de dados para determinar o tipo de dados que o Windows Media Player fornecerá no buffer de entrada. Se um método como **GetInputType** recuperar as informações do tipo de mídia, o plug-in deverá copiar o endereço da variável de membro que contém a estrutura do **\_ \_ tipo de mídia DMO** para o ponteiro fornecido pelo Windows Media Player na lista de parâmetros.

O Windows Media Player usa principalmente dois membros da estrutura de **\_ \_ tipo de mídia DMO** :

-   **majortype**: um GUID (identificador global exclusivo) que especifica a categoria geral da mídia, como áudio ou vídeo.
-   **subtipo**: um GUID que especifica uma descrição mais detalhada da mídia, como áudio PCM.

Essas GUIDs podem ser encontradas no cabeçalho chamado UUIDs. h, que está incluído com o SDK do Windows.

Métodos como **GetInputSizeInfo** fornecem informações ao Windows Media Player sobre a quantidade de memória necessária para alocar os buffers de processamento. Métodos como **GetStreamCount** e **GetOutputStreamInfo** fornecem informações para o Windows Media Player sobre o número e o caractere dos fluxos com suporte pelo plug-in do DSP.

**GetInputMaxLatency** e **SetInputMaxLatency** são implementados pelo DMOs em casos especiais. Plug-ins de DSP do Windows Media Player devem retornar E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especificam ou recuperam informações de estado

Esses são os métodos que o Windows Media Player chama para obter ou definir valores relacionados ao estado atual do plug-in. Esses métodos incluem:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** e **GetOutputCurrentType** usam a estrutura do **\_ \_ tipo de mídia DMO** para retornar informações ao Windows Media Player sobre os tipos de mídia definidos anteriormente para os fluxos de entrada e saída. **GetInputStatus** retorna um sinalizador que informa ao Windows Media Player se o plug-in do DSP pode aceitar dados de entrada.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que lidam com buffer e processando dados

Esses são os métodos que o Windows Media Player chama para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital. Esses métodos incluem:

-   **AllocateStreamingResources**
-   **Descontinuidade**
-   **Liberar**
-   **FreeStreamingResources**
-   **Bloquear**
-   **ProcessInput**
-   **ProcessOutput**

O Windows Media Player chama **AllocateStreamingResources** e **FreeStreamingResources** para fornecer o plug-in do DSP com uma oportunidade de configurar ou liberar os buffers adicionais que o plug-in pode exigir para processamento interno.

Os plug-ins do DSP do Windows Media Player não precisam usar o método de **descontinuidade** do DMO.

O Windows Media Player chama **flush** para direcionar o plug-in do DSP para liberar todos os dados armazenados em buffer internamente. O plug-in deve liberar todas as referências às interfaces **IMediaBuffer** , limpar quaisquer valores que especifiquem o carimbo de data/hora ou o tamanho da amostra para o buffer de mídia e reinicializar todos os Estados internos que dependem do conteúdo do exemplo de mídia.

O Windows Media Player chama ProcessInput para passar um ponteiro para uma interface **IMediaBuffer** para o plug-in do DSP. Essa interface fornece acesso ao buffer de entrada alocado pelo Windows Media Player para fornecer dados ao plug-in. Subseqüentemente, o Windows Media Player chama **ProcessOutput** para passar um ponteiro para uma interface **IMediaBuffer** que fornece acesso ao buffer de saída alocado pelo Windows Media Player para receber os dados processados do plug-in do DSP.

A interface **IMediaObject** inclui um método chamado **Lock**. Esse método foi projetado para adquirir ou liberar um bloqueio no DMO para manter o DMO serializado ao executar várias operações. A versão de **IMediaObject:: Lock** no código do assistente substitui a implementação da ATL do **bloqueio**. Como o Windows Media Player serializa chamadas feitas à interface DMO de um plug-in DSP, a implementação do **bloqueio** simplesmente retorna S \_ OK. Para obter detalhes sobre como criar um DMO multithread, consulte a seção DirectShow do SDK do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces necessárias**](required-interfaces.md)
</dt> </dl>

 

 




