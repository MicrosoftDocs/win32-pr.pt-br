---
description: Visão geral das considerações de Threading ao usar a API (interface de programação de aplicativo) do StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Considerações de threading para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ac95fdf0e74e30c83a437b6ed573d03bb2c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828474"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Considerações de threading para a API StylusInput

O objeto [**RealTimeStylus**](realtimestylus-class.md) foi projetado para fornecer acesso em tempo real ao fluxo de dados da caneta eletrônica. Plug-ins, objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) podem ser adicionados a um objeto **RealTimeStylus** . Plug-ins síncronos são geralmente chamados diretamente pelo objeto **RealTimeStylus** em um thread de alta prioridade, enquanto plug-ins assíncronos são geralmente chamados no thread da interface do usuário do aplicativo. Crie ou use plug-ins síncronos para tarefas que exigem acesso em tempo real ao fluxo de dados e são de cálculo computacional, como a filtragem de pacotes. Crie ou use plug-ins assíncronos para tarefas que não exigem acesso em tempo real ao fluxo de dados, como a coleta de tinta.

Como os dados de plug-in para a coleção de plug-ins assíncrono do objeto [**RealTimeStylus**](realtimestylus-class.md) são enfileirados, plug-in assíncronos podem receber dados antes de receber uma chamada para seu método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , mas depois que o objeto **RealTimeStylus** é desabilitado. Observe que alguns dos métodos e propriedades do objeto **RealTimeStylus** geram uma exceção se o objeto **RealTimeStylus** está desabilitado.

Os métodos de interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) a seguir podem chamar em um thread diferente do thread de dados da caneta eletrônica.

-   Os métodos [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) são chamados no thread que atualiza a propriedade [Enabled](/previous-versions/ms585380(v=vs.100)) do objeto [**RealTimeStylus**](realtimestylus-class.md) ou que adiciona ou remove o plug-in enquanto o objeto **RealTimeStylus** está habilitado.
-   O método [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) é chamado no thread que chama o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) do objeto [**RealTimeStylus**](realtimestylus-class.md) .
-   O método de [erro](/previous-versions/ms824754(v=msdn.10)) é chamado no thread no qual o plug-in síncrono está em execução quando gera uma exceção.

Para interagir com seu aplicativo a partir de um plug-in síncrono, use o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) do objeto [**RealTimeStylus**](realtimestylus-class.md) e manipule os dados da caneta personalizada em um dos seus plug-ins assíncronos. Se você fizer uma chamada síncrona para outro thread de um plug-in síncrono, poderá bloquear o objeto **RealTimeStylus** e, portanto, bloquear a coleta de tinta.

Determinadas tarefas podem ser computacionalmente exigentes, ainda assim exigem acesso em tempo real ao fluxo de dados da caneta do Tablet, como para o reconhecimento de gestos com vários traços. As APIs StylusInput fornecem um modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata que permite que você use dois objetos **RealTimeStylus** , cada um chamando seus plug-ins síncronos de threads diferentes. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

> [!Note]  
> Não é possível anexar o objeto [**RealTimeStylus**](realtimestylus-class.md) a uma janela ou controle em um processo diferente.

 

Para obter mais informações sobre considerações de threading para o Tablet PC em geral, consulte [considerações de Threading do Tablet PC](tablet-pc-threading-considerations.md)

 

 
