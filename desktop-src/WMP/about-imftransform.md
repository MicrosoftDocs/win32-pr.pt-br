---
title: Sobre IMFTransform
description: Sobre IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player plug-ins,interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins DSP
- Windows Media Player plug-ins, interface IMFTransform
- plug-ins, interface IMFTransform
- plug-ins de processamento de sinal digital, interface IMFTransform
- Plug-ins DSP, interface IMFTransform
- Interface IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903576"
---
# <a name="about-imftransform"></a>Sobre IMFTransform

A interface **IMFTransform** é uma das interfaces que devem ser implementadas por um plug-in DSP de modo duplo. Windows Media Player chama os métodos da interface **IMFTransform** para fornecer dados ao plug-in e recuperar dados processados de volta do plug-in. Para ver a documentação completa da interface **IMFTransform,** consulte Media Foundation seção do SDK do Windows.

Os métodos de **IMFTransform** podem ser categorizados da seguinte forma.

## <a name="methods-that-handle-format-negotiation"></a>Métodos que lidam com a negociação de formato

Windows Media Player chama os métodos a seguir para obter informações sobre os formatos de dados com suporte pelo plug-in.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **Setinputtype**
-   **Setoutputtype**
-   **Getattributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especificam ou recuperam informações de estado

Windows Media Player chama os métodos a seguir para obter ou definir valores relacionados ao estado atual do plug-in.

-   **Setinputtype**
-   **Setoutputtype**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType e** **SetOutputType** são usados tanto para negociação de formato quanto para especificar e recuperar informações de estado.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que lidam com o buffer e o processamento de dados

Windows Media Player chama os métodos a seguir para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital.

-   **ProcessInput**
-   **Processoutput**
-   **Processmessage**
-   **Processevent**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces necessárias**](required-interfaces.md)
</dt> </dl>

 

 




