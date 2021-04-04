---
description: A classe RealTimeStylus faz parte das APIs (interfaces de programação de aplicativo) do StylusInput. As seções a seguir descrevem os principais elementos da classe RealTimeStylus e as APIs StylusInput.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Trabalhando com a classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647382"
---
# <a name="working-with-the-realtimestylus-class"></a>Trabalhando com a classe RealTimeStylus

A classe [**RealTimeStylus**](realtimestylus-class.md) faz parte das APIs (interfaces de programação de aplicativo) do StylusInput. As seções a seguir descrevem os principais elementos da classe **RealTimeStylus** e as APIs StylusInput.

## <a name="instantiating-the-realtimestylus-class"></a>Instanciando a classe RealTimeStylus

Ao criar um objeto [**RealTimeStylus**](realtimestylus-class.md) , você tem a opção de anexá-lo a um identificador de janela ou a um controle. Anexar o objeto **RealTimeStylus** a um identificador de janela requer permissões adicionais. Para obter mais informações sobre essas permissões, consulte [considerações de confiança parcial para as APIs StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> Não é possível anexar o objeto [**RealTimeStylus**](realtimestylus-class.md) a uma janela ou controle em um processo diferente.

 

Se você usar o construtor padrão, criará um objeto [**RealTimeStylus**](realtimestylus-class.md) que só pode aceitar a entrada de outro objeto **RealTimeStylus** . Para obter mais informações sobre como conectar dois objetos **RealTimeStylus** , consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) implementa a interface [IDisposable](/dotnet/api/system.idisposable) .

## <a name="extending-the-realtimestylus-class"></a>Estendendo a classe RealTimeStylus

Para permitir que os plug-ins interajam com o fluxo de dados da caneta eletrônica, o objeto [**RealTimeStylus**](realtimestylus-class.md) mantém duas coleções de plug-in, que podem ser acessadas pelos métodos [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) e [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) em C++ e pelas propriedades [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) e [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) no código gerenciado. Você pode adicionar um plug-in chamando o método [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) ou [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) da coleção na propriedade apropriada. Para obter mais informações sobre como criar e usar plug-ins, consulte [plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Para obter informações sobre como decidir se deve criar um plug-in síncrono ou assíncrono para uma tarefa específica, consulte [considerações de threading para as APIs do StylusInput](threading-considerations-for-the-stylusinput-apis.md) e [considerações de desempenho para as APIs do StylusInput](performance-considerations-for-the-stylusinput-apis.md).

Plug-ins síncronos devem implementar a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e plug-ins assíncronos devem implementar a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Cada plug-in tem uma propriedade [**IStylusSyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) ou [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) . O objeto [**RealTimeStylus**](realtimestylus-class.md) chama apenas os métodos de notificação do plug-in para métodos em que o plug-in assinou. Para obter mais informações sobre os métodos de notificação, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) implementa a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . A única maneira de instanciar um objeto **RealTimeStylus** que aceita entrada de outro objeto **RealTimeStylus** é usar o construtor padrão e implementar o modelo **RealTimeStylus** em cascata. Para obter mais informações sobre como conectar dois objetos **RealTimeStylus** , consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) tem duas filas internas que transportam os dados da caneta do Tablet, a fila de entrada e a fila de saída. Os dados da caneta são convertidos em instâncias das classes no namespace [Microsoft. StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) . A lista a seguir descreve como o objeto **RealTimeStylus** manipula os dados da caneta eletrônica.

1.  O objeto [**RealTimeStylus**](realtimestylus-class.md) verifica primeiro os objetos de dados de plug-in em sua fila de entrada e, em seguida, do fluxo de dados da caneta eletrônica.
2.  O objeto [**RealTimeStylus**](realtimestylus-class.md) envia um objeto de dados de plug-in para os objetos em sua coleção de plug-ins síncrona. Cada plug-in síncrono pode adicionar dados à fila de entrada ou saída.
3.  Depois que o objeto de dados de plug-in for enviado a todos os membros da coleção de plug-ins síncronos, o objeto de dados de plug-in será colocado na fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) .
4.  O objeto [**RealTimeStylus**](realtimestylus-class.md) , em seguida, verifica o próximo objeto de dados de plug-in a ser processado.
5.  Embora a fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) contenha dados, o objeto **RealTimeStylus** envia um objeto de dados de plug-in de sua fila de saída para os objetos em sua coleção de plug-ins assíncrona. Cada plug-in assíncrono pode adicionar dados à fila de entrada ou de saída, mas como os plug-ins assíncronos são executados no thread da interface do usuário, os dados são adicionados à fila em relação aos dados da caneta atual que o objeto **RealTimeStylus** está processando e não em relação aos dados que o plug-in assíncrono está processando.

O diagrama a seguir ilustra o fluxo de dados da caneta do Tablet por meio do objeto [**RealTimeStylus**](realtimestylus-class.md) e de suas coleções de plug-ins.

![illustratiom mostrando o fluxo de dados da caneta do Tablet PC](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

Para obter mais informações sobre como os dados específicos são adicionados à fila e processados, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Veja a seguir um cenário mínimo para usar o objeto [**RealTimeStylus**](realtimestylus-class.md) em um formulário que coleta tinta.

1.  Crie um formulário que implemente a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Crie um objeto [**RealTimeStylus**](realtimestylus-class.md) anexado a um controle no formulário.
3.  Defina interesse nas notificações StylusDown, pacotes e StylusUp na propriedade [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) do formulário.
4.  Nos métodos [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) do formulário, adicione o código para lidar com as notificações de caneta para baixo, pacotes e canetas que são enviadas do objeto [**RealTimeStylus**](realtimestylus-class.md) do formulário.

Para obter uma amostra desse aplicativo, consulte o [exemplo de coleção de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Trabalhando com objetos do Tablet

Cada objeto [**RealTimeStylus**](realtimestylus-class.md) habilitado mantém uma lista de identificadores exclusivos para os objetos do [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) com os quais ele pode interagir. O objeto **RealTimeStylus** expõe dois métodos para converter entre o identificador exclusivo e o objeto do **Tablet** : os métodos [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) e [**GetTabletFromTabletContextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) .

O objeto [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) (em código gerenciado) contém uma propriedade [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) e uma estrutura [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) que descreve o intervalo, a resolução e as unidades da propriedade para um objeto de [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) específico. O método [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) do objeto [**RealTimeStylus**](realtimestylus-class.md) retorna uma matriz de GUIDs (identificadores globalmente exclusivos) para as propriedades de pacote que o objeto **RealTimeStylus** encaminha para seus plug-ins quando essas propriedades de pacote estão disponíveis. Para modificar o conjunto de propriedades de pacote que o objeto **RealTimeStylus** passa para seus plug-ins, chame o método [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) do objeto **RealTimeStylus** . O método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (no código gerenciado) do objeto **RealTimeStylus** usa um identificador de Tablet exclusivo e retorna uma coleção de objetos [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10)) . Essas propriedades de pacote representam o subconjunto de propriedades com suporte pelo Tablet que são retornadas pelo método **GetDesiredPacketDescription** .

Para obter uma lista dos GUIDs de propriedade de pacote padrão, consulte a classe [Constants PacketPropertyGuids](packetpropertyguids-constants.md) .

## <a name="special-considerations"></a>Considerações especiais

A lista a seguir descreve outros pontos a serem levados em consideração ao usar o objeto [**RealTimeStylus**](realtimestylus-class.md) com um objeto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

-   O método [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) só pode ser chamado enquanto o objeto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) estiver desabilitado. O objeto [**RealTimeStylus**](realtimestylus-class.md) pode modificar a lista de propriedades de pacote desejadas; Portanto, chame o método [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) após a chamada para o método **SetDesiredPacketDescription** para determinar quais propriedades de pacote o objeto **RealTimeStylus** pode encaminhar para seus plug-ins. Um Tablet só é garantido para dar suporte aos valores **X**, **Y** e **PacketStatus** para o [pacoteproperty](packetproperty-guids.md). Portanto, seu design de plug-ins pode precisar considerar o recebimento de menos Propriedades de pacote do que o desejado.
-   O método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (para código gerenciado) só pode ser chamado enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado. Como a notificação pode ser enviada para os plug-ins assíncronos depois que o objeto **RealTimeStylus** tiver sido desabilitado, talvez seja necessário armazenar em cache as informações de cada objeto do [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . O método GetTabletPropertyDescriptionCollection retorna uma lista das propriedades de pacote desejadas que são suportadas pelo Tablet especificado.
-   Quando o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, cada plug-in recebe uma chamada para seu método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) . O objeto [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) passado na notificação contém uma coleção de identificadores de contexto para os tablets disponíveis no momento em que o objeto **RealTimeStylus** está habilitado.
-   Quando um tablet que o objeto [**RealTimeStylus**](realtimestylus-class.md) pode usar é adicionado ou removido do Tablet PC enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** notifica seus plug-ins de que um objeto do [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) foi adicionado ou removido. Para obter mais informações, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Trabalhando com canetas do Tablet

O objeto [**RealTimeStylus**](realtimestylus-class.md) passa informações sobre a caneta eletrônica para seus plug-ins em vários métodos de notificação. As informações sobre a caneta eletrônica são representadas por um objeto [Stylus](/previous-versions/ms824824(v=msdn.10)) , obtidos pelo método [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) . Esse objeto é uma representação da caneta eletrônica no momento em que os dados foram coletados. Como os plug-ins recebem os dados da caneta eletrônica como parte do fluxo de dados da caneta eletrônica, os plug-ins devem usar as informações no objeto Stylus em vez de verificar o estado atual de uma caneta eletrônica específica por meio da classe [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Para obter informações sobre como a caneta eletrônica e os dados do botão da caneta eletrônica são passados para plug-ins, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Para obter uma matriz dos objetos de [caneta](/previous-versions/ms824824(v=msdn.10)) que o objeto [**RealTimeStylus**](realtimestylus-class.md) encontrou desde a última vez que ele foi habilitado, use o método [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) do objeto **RealTimeStylus** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[O modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerações de confiança parcial para as APIs StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
