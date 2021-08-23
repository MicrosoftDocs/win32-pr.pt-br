---
description: Um plug-in de processador dinâmico é um objeto que exibe os dados da caneta do Tablet em tempo real conforme são manipulados pelo objeto RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Plug-ins Dynamic-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6426dfc9f1dae8561802d2cf6c5613fb786600504cc8600046c4df781239abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092673"
---
# <a name="dynamic-renderer-plug-ins"></a>Plug-ins Dynamic-Renderer

Um plug-in de processador dinâmico é um objeto que exibe os dados da caneta do Tablet em tempo real conforme são manipulados pelo objeto [**RealTimeStylus**](realtimestylus-class.md) . Posteriormente, para eventos como uma atualização de formulário, o plug-in de processador dinâmico ou um plug-in de coletor de tinta pode redesenhar a tinta.

## <a name="the-dynamicrenderer-object"></a>O objeto DynamicRenderer

O objeto [**RealTimeStylus**](realtimestylus-class.md) implementa a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) renderiza a tinta em tempo real, pois ela está sendo desenhada. Quando o método [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) é chamado enquanto o objeto **DynamicRenderer** está habilitado, o objeto **DynamicRenderer** redesenha o traço que está sendo coletado no momento. A propriedade [**habilitada**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) do objeto **DynamicRenderer** é inicialmente definida como **false**.

> [!Note]  
> ao chamar o método de [**atualização**](/previous-versions/ms826370(v=msdn.10)) do objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) de dentro de um manipulador de eventos [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) em código gerenciado, defina a propriedade [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) do objeto **DynamicRenderer** como a propriedade [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) do objeto [painteventargs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) .

 

O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) pode armazenar temporariamente dados de tinta em cache. Para usar esse recurso em código gerenciado, defina a propriedade [EnableDataCache](/previous-versions/ms826349(v=msdn.10)) como **true**. Quando o objeto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) recebe uma chamada para seu método [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) , ele armazena em cache os dados de traço e adiciona dados da caneta personalizada à fila de entrada em resposta ao objeto [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) para o traço. A propriedade [CustomDataId](/previous-versions/ms824749(v=msdn.10)) do objeto [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) é definida como o valor [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) e a propriedade data do objeto **CustomStylusData** contém um objeto DynamicRendererCachedData. Chame o método [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) do objeto **DynamicRenderer** depois que o traço tiver sido coletado e puder ser processado estaticamente. Quando o método [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) é chamado enquanto o objeto **DynamicRenderer** está habilitado, o objeto **DynamicRenderer** redesenha todos os traços armazenados em cache. Quando a propriedade [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) é definida como **false**, os dados de traço armazenados em cache são excluídos.

O diagrama a seguir ilustra como o objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) adiciona dados aos dados da caneta eletrônica quando a propriedade [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) do objeto **DynamicRenderer** é definida.

![ilustração mostrando o fluxo de dados DynamicRenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

Neste diagrama, o círculo "SD" representa um objeto [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) e os círculos "P" representam os objetos de [**pacotes**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronas. O círculo "SU" representa um objeto [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e, em seguida, colocado na fila de saída. Os círculos com letra "DR" representam os dados da caneta personalizada que são adicionados à fila de entrada pelo plug-in [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) em resposta à notificação de caneta para cima associada a "su". Os dados da caneta personalizada "DR" são passados para os plug-ins síncronos e, em seguida, para a fila de saída antes de os próximos dados da caneta do Tablet serem processados. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados. Também representado no diagrama é o plug-in do coletor de tinta que chama o método [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) do objeto **DynamicRenderer** para liberar os dados de traço armazenados em cache após o plug-in de coleta de tinta ter processado o traço.

### <a name="special-considerations"></a>Considerações especiais

A lista a seguir descreve outros pontos a serem levados em consideração ao usar o objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) .

-   Você não deve anexar um objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a mais de um objeto [**RealTimeStylus**](realtimestylus-class.md) . Quando dois objetos **RealTimeStylus** aos quais o objeto **DynamicRenderer** está anexado são habilitados, ocorre o seguinte.

    -   O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) gera uma exceção em resposta à segunda chamada para seu método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) .
    -   O segundo objeto [**RealTimeStylus**](realtimestylus-class.md) que foi habilitado gera um objeto de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) e notifica os plug-ins restantes em suas coleções de plug-in do erro.
    -   O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) interrompe a renderização de dados da caneta do Tablet.

-   O objeto [**RealTimeStylus**](realtimestylus-class.md) gera uma exceção quando seu método [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) é chamado com o parâmetro *GUID* definido como o GUID (identificador global exclusivo) DynamicRendererCachedDataGuid.
-   O objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) é implementado como um wrapper Component Object Model (com) e você não pode chamar seus métodos de interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) diretamente. Para obter mais informações sobre a operação COM e o objeto [**RealTimeStylus**](realtimestylus-class.md) , consulte [notas de implementação para as APIs StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Renderização personalizada

Você pode criar seu próprio plug-in de processamento dinâmico criando um plug-in síncrono que assina o [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), os [**pacotes**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e as notificações do [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) . Seu plug-in pode renderizar o traço conforme ele está sendo desenhado. Essa pode ser uma maneira de implementar uma ferramenta de seleção que usa uma caixa de seleção de forma livre ou de seleção, por exemplo.

 

 
