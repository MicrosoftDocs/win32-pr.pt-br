---
description: O Tablet PC inclui a tecnologia para interagir com os dados da caneta do Tablet enquanto eles estão sendo coletados.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acessando e manipulando a entrada da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756519"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Acessando e manipulando a entrada da caneta

O Tablet PC inclui a tecnologia para interagir com os dados da caneta do Tablet enquanto eles estão sendo coletados. A classe [**RealTimeStylus**](realtimestylus-class.md) faz parte das interfaces de programação de aplicativo (API) do StylusInput, que fornecem acesso ao fluxo de dados da caneta do Tablet. Essas APIs permitem capturar, interromper e modificar o fluxo independentemente da renderização e da coleta de tinta.

As APIs StylusInput são projetadas para:

-   Forneça acesso em tempo real ao fluxo de dados da caneta eletrônica.
-   Mantenha o thread da interface do usuário para bloquear a renderização de tinta dinâmica ao enfileirar os dados de pacote no thread da interface do usuário e fazer uma coleta de tinta thread único.
-   Aumente o desempenho e reduza o uso geral do thread usando o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) , o controle [InkPicture](inkpicture-control-reference.md) ou o controle [InkEdit](inkedit-control-reference.md) para coletar tinta.

As APIs StylusInput não foram projetadas para trabalhar com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) , o controle [InkPicture](inkpicture-control-reference.md) ou o controle [InkEdit](inkedit-control-reference.md) .

Quando você precisa interagir diretamente com o fluxo de dados da caneta do Tablet ou quando seu aplicativo pode bloquear a escrita em tempo real, use o objeto [**RealTimeStylus**](realtimestylus-class.md) . Use o controle objeto [**InkCollector**](inkcollector-class.md) , objeto [**InkOverlay**](inkoverlay-class.md) , controle [InkPicture](inkpicture-control-reference.md) ou [InkEdit](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornecer o comportamento de que você precisa.

## <a name="in-this-section"></a>Nesta seção

As seções a seguir descrevem os elementos das APIs StylusInput:

-   [Arquitetura das APIs do StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Trabalhando com as APIs do StylusInput](working-with-the-stylusinput-apis.md)
    -   [Trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
    -   [Plug-ins de processamento dinâmico](dynamic-renderer-plug-ins.md)
    -   [Plug-ins do Recognizer](recognizer-plug-ins.md)
-   [Considerações ao usar as APIs StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Considerações de design para as APIs StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)

-   [Considerações de tratamento de erro para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Considerações de desempenho para as APIs StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Considerações de confiança parcial para as APIs StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Exemplo de coleção de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



