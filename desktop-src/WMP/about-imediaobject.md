---
title: Sobre IMediaObject
description: Sobre IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player plug-ins,interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins DSP
- Windows Media Player plug-ins, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de processamento de sinal digital, interface IMediaObject
- Plug-ins DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dbf44a527d61d924045a4bcceded5d90bb174fef608e3b7667338e99aa1efe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583903"
---
# <a name="about-imediaobject"></a>Sobre IMediaObject

A interface **IMediaObject** é a interface necessária para DMOs. **IMediaObject** contém os métodos que um plug-in DSP do Windows Media Player usa para obter dados do Windows Media Player, processar os dados e retornar os dados processados para Windows Media Player. Para ver a documentação completa da interface **IMediaObject,** consulte a DirectShow do SDK do Windows.

Os métodos de **IMediaObject** podem ser categorizados da seguinte forma:

## <a name="methods-that-handle-format-negotiation"></a>Métodos que lidam com a negociação de formato

Esses são os métodos que Windows Media Player chamadas para obter informações sobre os formatos de dados com suporte pelo plug-in. Esses métodos incluem:

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **Getoutputtype**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **Setinputtype**
-   **Setoutputtype**

Vários desses métodos, como **GetInputType** e **SetInputType,** usam a estrutura **DMO MEDIA \_ \_ TYPE** para descrever o formato dos dados usados por um fluxo. Quando Windows Media Player chama esses métodos, ele fornece um ponteiro para uma estrutura **DMO \_ MEDIA \_ TYPE.** Se um método como **SetInputType** especificar as informações de tipo de mídia, o plug-in deverá copiar a estrutura **DMO MEDIA \_ \_ TYPE** para uma variável de membro e inspecionar seus membros de dados para determinar o tipo de dados que o Windows Media Player fornecerá no buffer de entrada. Se um método como **GetInputType** recuperar as informações de tipo de mídia, o plug-in deverá copiar o endereço da variável membro que contém a estrutura **DMO MEDIA \_ \_ TYPE** para o ponteiro fornecido pelo Windows Media Player na lista de parâmetros.

Windows Media Player usa principalmente dois membros da estrutura **DMO \_ MEDIA \_ TYPE:**

-   **majortype:** um GUID (identificador global exclusivo) que especifica a categoria geral da mídia, como áudio ou vídeo.
-   **subtipo**: um GUID que especifica uma descrição mais detalhada da mídia, como áudio PCM.

Esses GUIDs podem ser encontrados no header chamado uuids.h, que está incluído no SDK Windows aplicativo.

Métodos como **GetInputSizeInfo** fornecem informações para Windows Media Player sobre a memória necessária para alocar os buffers de processamento. Métodos como **GetStreamCount** e **GetOutputStreamInfo** fornecem informações para Windows Media Player sobre o número e o caractere dos fluxos com suporte pelo plug-in DSP.

**GetInputMaxLatency** e **SetInputMaxLatency** são implementados por DMOs em casos especiais. Windows Media Player Os plug-ins DSP devem retornar E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especificam ou recuperam informações de estado

Esses são os métodos que Windows Media Player chamadas para obter ou definir valores relacionados ao estado atual do plug-in. Esses métodos incluem:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** e **GetOutputCurrentType** usam a estrutura **DMO MEDIA \_ \_ TYPE** para retornar informações Windows Media Player sobre os tipos de mídia definidos anteriormente para os fluxos de entrada e saída. **GetInputStatus retorna** um sinalizador que Windows Media Player se o plug-in DSP pode aceitar dados de entrada.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que lidam com o buffer e o processamento de dados

Esses são os métodos que Windows Media Player chamadas para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital. Esses métodos incluem:

-   **Allocatestreamingresources**
-   **Descontinuidade**
-   **Liberar**
-   **FreeStreamingResources**
-   **Bloquear**
-   **ProcessInput**
-   **Processoutput**

Windows Media Player chama **AllocateStreamingResources** e **FreeStreamingResources** para fornecer ao plug-in DSP a oportunidade de configurar ou liberar quaisquer buffers adicionais que o plug-in possa exigir para processamento interno.

Windows Media Player Os plug-ins DSP não precisam usar o método DMO **Descontinuidade.**

Windows Media Player **chama Flush para** direcionar o plug-in DSP para liberar todos os dados armazenados em buffer internamente. O plug-in deve liberar quaisquer referências às interfaces **IMediaBuffer,** limpar quaisquer valores que especifiquem o carimbo de data/hora ou o tamanho da amostra para o buffer de mídia e reinicializar todos os estados internos que dependem do conteúdo do exemplo de mídia.

Windows Media Player processInput para passar um ponteiro para uma interface **IMediaBuffer** para o plug-in DSP. Essa interface fornece acesso ao buffer de entrada alocado pelo Windows Media Player para fornecer dados ao plug-in. Windows Media Player subsequentemente chama **ProcessOutput** para passar um ponteiro para uma interface **IMediaBuffer** que fornece acesso ao buffer de saída alocado pelo Windows Media Player para receber os dados processados do plug-in do DSP.

A interface **IMediaObject** inclui um método chamado **Lock**. Esse método foi projetado para adquirir ou liberar um bloqueio no DMO para manter o DMO serializado ao executar várias operações. A versão de **IMediaObject::Lock** no código do assistente substitui a implementação da ATL de **Bloquear**. Como Windows Media Player serializa chamadas feitas à interface DMO de um plug-in DSP, a implementação de **Bloqueio** simplesmente retorna S \_ OK. Para obter detalhes sobre como criar um DMO multithread, consulte a seção DirectShow do SDK do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces necessárias**](required-interfaces.md)
</dt> </dl>

 

 




