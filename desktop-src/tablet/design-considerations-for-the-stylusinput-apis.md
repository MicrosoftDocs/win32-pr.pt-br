---
description: Visão geral das considerações para criar um aplicativo que usa as APIs (interfaces de programação de aplicativo) do StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Considerações de design para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd97a5bad203dd23611acf3d6cb07bead1e1744a10b9ac39afe8a53e65597d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936626"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Considerações de design para a API StylusInput

Veja a seguir as considerações de design para a API do StylusInput.

-   Você pode atualizar a propriedade [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) do objeto [**RealTimeStylus**](realtimestylus-class.md) e a propriedade [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) do objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) enquanto a caneta está inativa. Isso pode ser útil quando você deseja ter uma área de desenho dinâmica enquanto o aplicativo está coletando tinta.
-   Para otimizar a reutilização e a manutenção do código de plug-in, os plug-ins não devem fazer chamadas diretamente para o aplicativo, mas devem usar o [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) (objeto [CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) no código gerenciado) para se comunicar com o aplicativo.
-   As coleções de plug-ins do objeto [**RealTimeStylus**](realtimestylus-class.md) são ordenadas. A posição relativa dos seus plug-ins nessas coleções pode ser muito importante. Por exemplo, um plug-in que modifica informações de pacote provavelmente deve ser adicionado à coleção de plug-ins síncrona antes de um plug-in de processador dinâmico.
-   A capacidade de adicionar dados da caneta personalizada ao fluxo de dados da caneta do Tablet deve ser usada com moderação. Use esse recurso somente se outro plug-in precisar receber essas informações como parte do fluxo de dados. Além disso, evite adicionar dados da caneta personalizada em resposta a outros dados da caneta personalizada que entram no plug-in, pois isso pode criar um loop infinito.
-   As coleções de plug-ins podem ser modificadas enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; no entanto, isso pode tornar o comportamento do seu aplicativo mais difícil de prever. Quando um plug-in é adicionado enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o Microsoft. StylusInput. IStylusSyncPlugin do plug-in. Método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (o método [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) no código gerenciado). Quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** chama o método [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) do plug-in (o método [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) no código gerenciado). Isso permite que o plug-in Mantenha seu estado adequado sem precisar verificar a propriedade [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) do objeto **RealTimeStylus** . Quando um plug-in é adicionado enquanto o objeto **RealTimeStylus** está habilitado, os dados de plug-in que o plug-in recebe podem não conter informações suficientes para estabelecer adequadamente o contexto dos dados iniciais. Por exemplo, o plug-in recém-adicionado pode começar a receber dados de pacote de uma caneta que está em um traço intermediário. Da mesma forma, quando um plug-in é removido enquanto o objeto **RealTimeStylus** está habilitado, os dados de plug-in que o plug-in recebeu podem não ser suficientes para concluir o processamento dos dados.
    > [!Note]  
    > Para a estabilidade geral, redefina o estado interno de um plug-in quando o método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) ou [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) for chamado.

     

-   O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção se um plug-in modifica a coleção de plug-ins à qual está anexada. Isso ocorre apenas quando o plug-in faz isso enquanto está sendo chamado pelo objeto **RealTimeStylus** como um membro dessa coleção.

 

 
