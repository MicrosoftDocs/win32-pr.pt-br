---
title: Sobre o IMFTransform
description: Sobre o IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IMFTransform
- plug-ins, interface IMFTransform
- plug-ins de processamento de sinal digital, interface IMFTransform
- Plug-ins do DSP, interface IMFTransform
- Interface IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781289"
---
# <a name="about-imftransform"></a>Sobre o IMFTransform

A interface **IMFTransform** é uma das interfaces que devem ser implementadas por um plug-in DSP de modo duplo. O Windows Media Player chama os métodos da interface **IMFTransform** para fornecer dados ao plug-in e recuperar dados processados de volta do plug-in. Para obter a documentação completa da interface **IMFTransform** , consulte a seção Media Foundation do SDK do Windows.

Os métodos de **IMFTransform** podem ser categorizados da seguinte maneira.

## <a name="methods-that-handle-format-negotiation"></a>Métodos que manipulam a negociação de formato

O Windows Media Player chama os seguintes métodos para obter informações sobre os formatos de dados com suporte pelo plug-in.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **Setoutputtypetype**
-   **Falha GetAttributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especificam ou recuperam informações de estado

O Windows Media Player chama os seguintes métodos para obter ou definir valores relacionados ao estado atual do plug-in.

-   **SetInputType**
-   **Setoutputtypetype**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType** e **setoutputtypetype** são usados para a negociação de formato e para especificar e recuperar informações de estado.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que lidam com buffer e processando dados

O Windows Media Player chama os seguintes métodos para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces necessárias**](required-interfaces.md)
</dt> </dl>

 

 




