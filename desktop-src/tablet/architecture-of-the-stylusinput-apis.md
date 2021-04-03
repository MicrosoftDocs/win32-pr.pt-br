---
description: As APIs do StylusInput permitem que você interaja com o fluxo de dados da caneta do Tablet. Para interagir com o fluxo de dados, adicione um objeto RealTimeStylus ao seu aplicativo e adicione plug-ins ao objeto RealTimeStylus.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Arquitetura das APIs do StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeda6a6a0269e8306aed6a6b6de4c1bbe33bc46f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091745"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Arquitetura das APIs do StylusInput

As APIs do StylusInput permitem que você interaja com o fluxo de dados da caneta do Tablet. Para interagir com o fluxo de dados, adicione um objeto [**RealTimeStylus**](realtimestylus-class.md) ao seu aplicativo e adicione plug-ins ao objeto **RealTimeStylus** .

Dois plug-ins são fornecidos nas APIs do StylusInput. O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implementa a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . O objeto **DynamicRenderer** renderiza a tinta em tempo real, pois ela está sendo desenhada. O objeto [**GestureRecognizer**](gesturerecognizer-class.md) implementa as interfaces **IStylusSyncPlugin** e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . O objeto **GestureRecognizer** reconhece os gestos do aplicativo.

## <a name="definitions"></a>Definições

Os termos a seguir são usados nas seções que descrevem as APIs StylusInput:

Plug-in síncrono

Uma classe que implementa a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Plug-ins síncronos são geralmente chamados diretamente pelo objeto [**RealTimeStylus**](realtimestylus-class.md) .

Plug-in assíncrono

Uma classe que implementa a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Plug-ins assíncronos são geralmente chamados no thread da interface do usuário do aplicativo.

Coleção de plug-ins síncrona

Uma coleção [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) , que é uma coleção ordenada de objetos [IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10)) . Uma coleção de plug-ins síncrona geralmente se refere à coleção atribuída à propriedade [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) de um objeto [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Somente plug-ins síncronos podem ser adicionados a uma coleção de plug-in síncrona.

Coleção de plug-ins assíncrono

Uma coleção [StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10)) , que é uma coleção ordenada de objetos [IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10)) . Uma coleção de plug-ins assíncrona geralmente se refere à coleção atribuída à propriedade [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) de um objeto [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Somente plug-ins assíncronos podem ser adicionados a uma coleção de plug-in assíncrona.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Plug-ins síncronos e assíncronos

O objeto [**RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados de uma caneta eletrônica. Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real para o fluxo de dados e são, de modo computacional, desexigentes, como para filtragem de pacotes. Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como para criar e armazenar traços em um objeto [**InkDisp**](inkdisp-class.md) .

Determinadas tarefas podem ser computacionalmente exigentes, mas exigem acesso em tempo real ao fluxo de dados, como o reconhecimento de gestos com vários traços. Para atender a essas necessidades, as APIs StylusInput fornecem um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus** , cada um em execução em seu próprio thread. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

Para obter mais informações sobre como usar e criar plug-ins, consulte [trabalhando com as APIs StylusInput](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>O fluxo de dados da caneta do Tablet

O objeto [**RealTimeStylus**](realtimestylus-class.md) tem duas filas internas que transportam os dados da caneta do Tablet, a fila de entrada e a fila de saída. Os dados da caneta são convertidos em instâncias das classes no namespace [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . A lista a seguir descreve como o objeto **RealTimeStylus** manipula os dados da caneta eletrônica:

O objeto [**RealTimeStylus**](realtimestylus-class.md) verifica primeiro os objetos de dados de plug-in em sua fila de entrada e, em seguida, do fluxo de dados da caneta eletrônica.

O objeto [**RealTimeStylus**](realtimestylus-class.md) envia um objeto de dados de plug-in para os objetos em sua coleção de plug-ins síncrona. Cada plug-in síncrono pode adicionar dados à fila de entrada ou saída.

Depois que o objeto de dados de plug-in for enviado a todos os membros da coleção de plug-ins síncronos, o objeto de dados de plug-in será colocado na fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) .

O objeto [**RealTimeStylus**](realtimestylus-class.md) , em seguida, verifica o próximo objeto de dados de plug-in a ser processado.

Embora a fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) contenha dados, o objeto **RealTimeStylus** envia um objeto de dados de plug-in de sua fila de saída para os objetos em sua coleção de plug-ins assíncrona. Cada plug-in assíncrono pode adicionar dados à fila de entrada ou de saída. No entanto, como os plug-ins assíncronos são executados no thread da interface do usuário, os dados são adicionados à fila em relação aos dados da caneta atual que o objeto **RealTimeStylus** está processando e não em relação aos dados que o plug-in assíncrono está processando.

O diagrama a seguir ilustra o fluxo de dados da caneta do Tablet por meio do objeto [**RealTimeStylus**](realtimestylus-class.md) e de suas coleções de plug-ins.

![fluxo de dados da caneta do Tablet por meio do objeto RealTimeStylus e suas coleções de plug-ins](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

Neste diagrama, os círculos rotulados como "A" e "B" representam dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo rotulado como "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

Para obter mais informações sobre como os dados específicos são adicionados à fila e processados, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>As APIs StylusInput

As APIs StylusInput residem principalmente nos namespaces [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . No entanto, as APIs StylusInput também fazem referência a algumas classes no namespace [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) , como a classe [Tablet](/previous-versions/ms827783(v=msdn.10)) , a coleção [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) e as enumerações [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) e [SystemGesture](/previous-versions/ms827134(v=msdn.10)) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**RealTimeStylus**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Trabalhando com as APIs do StylusInput](working-with-the-stylusinput-apis.md)
</dt> <dt>

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
