---
description: O Tablet PC inclui tecnologia para interagir com dados de caneta de tablet à medida que eles estão sendo coletados.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acessando e manipulando a entrada da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452053"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Acessando e manipulando a entrada da caneta

O Tablet PC inclui tecnologia para interagir com dados de caneta de tablet à medida que eles estão sendo coletados. A [**classe RealTimeStylus**](realtimestylus-class.md) faz parte das API (interfaces de programação de aplicativo) StylusInput, que fornecem acesso ao fluxo de dados da caneta de tablet. Essas APIs permitem capturar, interromper e modificar o fluxo independentemente da renderização e coleta de tinta.

As APIs StylusInput foram projetadas para:

-   Forneça acesso em tempo real ao fluxo de dados da caneta de tablet.
-   Impedir que o thread de interface do usuário bloquee a renderização de tinta dinâmica enquera os dados de pacote no thread da interface do usuário e tornando a coleção de tintas single threaded.
-   Aumente o desempenho e reduza o uso geral do thread usando o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay,**](inkoverlay-class.md) o controle [InkPicture](inkpicture-control-reference.md) ou [o controle InkEdit](inkedit-control-reference.md) para coletar tinta.

As APIs StylusInput não foram projetadas para funcionar com o objeto [**InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay,**](inkoverlay-class.md) o [controle InkPicture](inkpicture-control-reference.md) ou [o controle InkEdit.](inkedit-control-reference.md)

Quando você precisar interagir diretamente com o fluxo de dados da caneta tablet ou quando seu aplicativo pode bloquear a tinta em tempo real, use o [**objeto RealTimeStylus.**](realtimestylus-class.md) Use o [**objeto InkCollector,**](inkcollector-class.md) o objeto [**InkOverlay,**](inkoverlay-class.md) o [controle InkPicture](inkpicture-control-reference.md) ou o [controle InkEdit](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornece o comportamento necessário.

## <a name="in-this-section"></a>Nesta seção

As seções a seguir descrevem elementos das APIs StylusInput:

-   [Arquitetura das APIs StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Trabalhando com as APIs StylusInput](working-with-the-stylusinput-apis.md)
    -   [Trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Plug-ins de coleta de tinta](ink-collection-plug-ins.md)
    -   [Plug-ins de renderização dinâmica](dynamic-renderer-plug-ins.md)
    -   [Plug-ins do Reconhecedor](recognizer-plug-ins.md)
-   [Considerações ao usar as APIs StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Considerações de design para as APIs StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)

-   [Considerações sobre tratamento de erros para as APIs StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Considerações de desempenho para as APIs StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Considerações de confiança parcial para as APIs StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Exemplo de coleção de tinta RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



