---
description: Visão geral das considerações de threading ao usar a API (interface de programação de aplicativo) StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Considerações de threading para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f9a26da86295a322d926278eda87388c0105132eafd2dfa3d7a9f6c6655e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819636"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Considerações de threading para a API StylusInput

O [**objeto RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta do tablet. Plug-ins, objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) podem ser adicionados a um **objeto RealTimeStylus.** Plug-ins síncronos geralmente são chamados diretamente pelo objeto **RealTimeStylus** em um thread de alta prioridade, enquanto plug-ins assíncronos geralmente são chamados no thread da interface do usuário do aplicativo. Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real ao fluxo de dados e são computacionalmente indesejáveis, como filtragem de pacotes. Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como coleta de tinta.

Como os dados de plug-in para a coleção de plug-ins assíncronos do objeto [**RealTimeStylus**](realtimestylus-class.md) estão na fila, os plug-ins assíncronos podem receber dados antes de receber uma chamada para seu [método RealTimeStylusDisabled,](/previous-versions/ms824774(v=msdn.10)) mas depois que o **objeto RealTimeStylus** é desabilitado. Observe que alguns dos métodos e propriedades do objeto **RealTimeStylus** lançarão uma exceção se o **objeto RealTimeStylus** estiver desabilitado.

Os métodos de interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) a seguir podem chamar em um thread diferente do thread de dados da caneta de tablet.

-   Os métodos [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) são chamados no thread que atualiza a propriedade [Enabled](/previous-versions/ms585380(v=vs.100)) do objeto [**RealTimeStylus**](realtimestylus-class.md) ou que adiciona ou remove o plug-in enquanto o **objeto RealTimeStylus** está habilitado.
-   O [método CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) é chamado no thread que chama o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) do objeto [**RealTimeStylus.**](realtimestylus-class.md)
-   O [método](/previous-versions/ms824754(v=msdn.10)) Error é chamado no thread no qual o plug-in síncrono está em execução quando ele lança uma exceção.

Para interagir com seu aplicativo de um plug-in síncrono, use o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) do objeto [**RealTimeStylus**](realtimestylus-class.md) e manipular os dados personalizados da caneta em um de seus plug-ins assíncronos. Se você fizer uma chamada síncrona para outro thread de um plug-in síncrono, poderá bloquear o **objeto RealTimeStylus** e, portanto, bloquear a coleta de tinta.

Determinadas tarefas podem ser computacionalmente exigentes, mas ainda exigem acesso em tempo real ao fluxo de dados da caneta tablet, como o reconhecimento de gestos multivalo. As APIs StylusInput fornecem um modelo [**realTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus,** cada um chamando seus plug-ins síncronos de threads diferentes. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte O modelo [RealTimeStylus](the-cascaded-realtimestylus-model.md)em cascata .

> [!Note]  
> Não é possível anexar [**o objeto RealTimeStylus**](realtimestylus-class.md) a uma janela ou controle em um processo diferente.

 

Para obter mais informações sobre considerações de threading para o tablet pc em geral, consulte [Considerações sobre threading de tablet](tablet-pc-threading-considerations.md)

 

 
