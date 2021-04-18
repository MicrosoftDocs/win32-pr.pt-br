---
description: Os plug-ins para a classe RealTimeStylus devem implementar a interface IStylusSyncPlugin ou IStylusAsyncPlugin, ou ambas.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Dados de plug-in e a classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372b3d297edbad6d339285f45e92118184fa2cfc
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104571411"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Dados de plug-in e a classe RealTimeStylus

Os plug-ins para a classe [**RealTimeStylus**](realtimestylus-class.md) devem implementar a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , ou ambas. Embora você precise implementar todos os métodos de interface de plug-in, seu plug-in recebe apenas chamadas em métodos sinalizados na propriedade plug-ins [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) .

Os métodos definidos nas interfaces usam objetos no namespace [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para passar os dados da caneta para os plug-ins. A tabela a seguir descreve os objetos de dados que são parâmetros nos métodos de notificação e lista o valor de [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) associado à notificação.



| Dados de plug-in                                                                                          | Valor de DataInterestMask     | Descrição                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Dados de aplicativo personalizados que um plug-in adiciona.<br/>                                                                                                                                                                                                 |
| [ErrorData](/previous-versions/ms824740(v=msdn.10))                                   | **Erro**                  | Informações de erro que o objeto [**RealTimeStylus**](realtimestylus-class.md) adiciona em resposta a uma exceção sem tratamento em um de seus plug-ins.<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Informações de pacote para o movimento da caneta enquanto a caneta está no ar acima do digitalizador.<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **Pacotes**                | Informações de pacote para o movimento da caneta enquanto a caneta está tocando no digitalizador.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Informações que o objeto [**RealTimeStylus**](realtimestylus-class.md) adiciona quando está sendo desabilitado.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informações que o objeto [**RealTimeStylus**](realtimestylus-class.md) adiciona quando está sendo habilitado.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Informações sobre o botão de caneta específico que está sendo pressionado.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informações sobre o botão de caneta específico que está sendo lançado.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | Informações de pacote para uma caneta à medida que a caneta é colocada em contato com o digitalizador.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informações sobre a caneta específica que está inserindo a área de entrada do objeto [**RealTimeStylus**](realtimestylus-class.md) ou inserindo o intervalo de detecção do digitalizador acima da área de entrada do objeto **RealTimeStylus** .<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Informações sobre a caneta específica que está deixando a área de entrada do objeto [**RealTimeStylus**](realtimestylus-class.md) ou deixando o intervalo de detecção do digitalizador acima da área de entrada do objeto **RealTimeStylus** .<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Informações de pacote para uma caneta à medida que a caneta é levantada do digitalizador.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Informações que o objeto [**RealTimeStylus**](realtimestylus-class.md) adiciona ao detectar um gesto do sistema.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | Informações sobre o objeto do [Tablet](/previous-versions/ms827783(v=msdn.10)) que está sendo adicionado.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Informações sobre o objeto do [Tablet](/previous-versions/ms827783(v=msdn.10)) que está sendo removido.<br/>                                                                                                                                              |



 

Para obter informações sobre como o objeto [**RealTimeStylus**](realtimestylus-class.md) manipula o fluxo de dados da caneta eletrônica, consulte [trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Interesse de dados

O objeto [**RealTimeStylus**](realtimestylus-class.md) verifica a propriedade [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) de um plug-in quando o plug-in é adicionado à coleção de plug-ins síncrono ou assíncrono do objeto **RealTimeStylus** . Portanto, você deve usar a propriedade DataInterest para assinar todas as notificações que essa instância do seu plug-in usa, no entanto, com pouca frequência, mas não com nenhuma das notificações que essa instância do seu plug-in nunca usa. Para notificações que seu plug-in usa apenas ocasionalmente, verifique primeiro o estado do seu plug-in no método de notificação e retorne se a notificação não for usada pelo seu plug-in em seu estado atual.

Um plug-in recebe apenas chamadas em métodos sinalizados na propriedade [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) do plug-in. Para obter mais informações sobre os possíveis valores da propriedade **Datainteresse** de um plug-in, consulte a enumeração [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .

## <a name="timing"></a>Timing

Os dados são enfileirados no objeto [**RealTimeStylus**](realtimestylus-class.md) antes de serem passados para os plug-ins na coleção plug-in assíncrona. A lista a seguir descreve algumas situações que talvez você precise considerar ao criar um plug-in assíncrono.

-   Quando o objeto [**RealTimeStylus**](realtimestylus-class.md) é desabilitado, o plug-in assíncrono pode receber outras notificações em fila antes de seu método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) ser chamado. Nessa situação, as chamadas do plug-in para alguns métodos e propriedades do objeto **RealTimeStylus** geram uma exceção. As informações relevantes para o seu plug-in devem ser armazenadas em cache quando o objeto **RealTimeStylus** está habilitado.
-   O método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) do objeto [**RealTimeStylus**](realtimestylus-class.md) pode remover informações da fila de saída. Portanto, plug-ins assíncronos não podem confiar no recebimento de todas as notificações relevantes.
-   Quando um objeto do [Tablet](/previous-versions/ms827783(v=msdn.10)) que está disponível para o objeto [**RealTimeStylus**](realtimestylus-class.md) é removido, o plug-in assíncrono pode receber a notificação da caneta enfileirada para o Tablet antes de seu método [TabletRemoved](/previous-versions/bb361092(v=vs.100)) ser chamado. Nessa situação, chamar o método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) do objeto **RealTimeStylus** não funciona. As informações relevantes para o seu plug-in devem ser armazenadas em cache quando o objeto **RealTimeStylus** está habilitado ou quando um novo tablet é adicionado.

Dependendo do seu aplicativo, você pode melhorar o desempenho ao desabilitar um objeto [**RealTimeStylus**](realtimestylus-class.md) . Quando a propriedade [habilitada](/previous-versions/ms824832(v=msdn.10)) do objeto **RealTimeStylus** é definida como **false**, os dados nas filas de entrada e saída são processados até que as filas estejam vazias. Você pode chamar o método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) do objeto **RealTimeStylus** para limpar as filas antes de desabilitar o objeto **RealTimeStylus** .

## <a name="enabled-and-disabled-data"></a>Dados habilitados e desabilitados

Quando o objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, cada plug-in recebe uma chamada para seu método [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) . O objeto **RealTimeStylusEnabledData** passado na notificação contém uma coleção de identificadores de contexto para os tablets disponíveis no momento em que o objeto **RealTimeStylus** está habilitado.

> [!Note]  
> Como os dados de plug-in para a coleção de plug-ins assíncrono do objeto [**RealTimeStylus**](realtimestylus-class.md) são enfileirados, plug-in assíncronos podem receber dados antes de receber uma chamada para seu método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , mas depois que o objeto **RealTimeStylus** é desabilitado. Observe que alguns dos métodos e propriedades do objeto **RealTimeStylus** geram uma exceção se o objeto **RealTimeStylus** está desabilitado.

 

O objeto [**RealTimeStylus**](realtimestylus-class.md) chama os métodos [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) no thread a partir do qual o objeto **RealTimeStylus** está habilitado ou do qual o plug-in síncrono é adicionado.

Em geral, adicione ou remova plug-ins enquanto o objeto [**RealTimeStylus**](realtimestylus-class.md) está desabilitado. Para obter mais informações sobre como adicionar e remover plug-ins para o objeto **RealTimeStylus** , consulte [plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Dados do Tablet

Quando um tablet que o objeto [**RealTimeStylus**](realtimestylus-class.md) pode usar é adicionado ou removido do Tablet PC enquanto o objeto **RealTimeStylus** está habilitado, o objeto **RealTimeStylus** notifica seus plug-ins de que um objeto do [Tablet](/previous-versions/ms827783(v=msdn.10)) foi adicionado ou removido. Cada objeto **RealTimeStylus** mantém uma lista de identificadores exclusivos para os objetos do Tablet com os quais ele pode interagir. O objeto **RealTimeStylus** tem dois métodos para converter entre o identificador exclusivo e o objeto do Tablet, os métodos [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) e [GetTabletFromTabletContextId](/previous-versions/ms825929(v=msdn.10)) .

> [!Note]  
> As informações sobre um Tablet não estarão mais disponíveis no objeto [**RealTimeStylus**](realtimestylus-class.md) depois que o Tablet for removido do Tablet PC.

 

## <a name="tablet-pen-data"></a>Dados da caneta do Tablet

O objeto [**RealTimeStylus**](realtimestylus-class.md) passa informações sobre a caneta eletrônica para seus plug-ins em vários métodos de notificação. As informações sobre a caneta eletrônica são representadas por um objeto [Stylus](/previous-versions/ms824824(v=msdn.10)) . Esse objeto é um instantâneo do estado da caneta eletrônica no momento em que os dados foram coletados. Como os plug-ins recebem os dados da caneta eletrônica como parte do fluxo de dados da caneta eletrônica, os plug-ins devem usar as informações no objeto Stylus em vez de verificar o estado atual de uma caneta eletrônica específica por meio da classe [cursor](/previous-versions/ms839521(v=msdn.10)) .

Cada objeto da [caneta](/previous-versions/ms824824(v=msdn.10)) contém o identificador de contexto do Tablet para o Tablet que gerou os dados.

## <a name="system-gesture-data"></a>Dados de gesto do sistema

O objeto [**RealTimeStylus**](realtimestylus-class.md) recebe dados sobre gestos do sistema conforme eles são reconhecidos pelo Tablet PC. A tabela a seguir descreve a ordem na qual os objetos [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) ocorrem no fluxo de dados da caneta eletrônica em relação a outros dados da caneta do Tablet.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a></th>
<th>Objetos que precedem o objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
<th>Objetos que vêm após o objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Toque</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>O objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>DoubleTap</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> , o objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para o gesto do sistema <strong>Tap</strong> e os objetos [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
<td>O segundo objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightTap</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> e o objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para o membro <strong>HoldEnter</strong> da enumeração <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure</a> .<br/></td>
<td>O objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>Arrastar</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>O objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightDrag</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>O objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>HoldEnter</strong></td>
<td>O objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>O objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/>
<blockquote>
[!Note]<br />
Esse gesto do sistema não será reconhecido se o usuário iniciar um gesto de sistema de <strong>arrastar</strong> ou <strong>RightDrag</strong> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoldLeave</strong></td>
<td>Não implementado.<br/></td>
<td>Não implementado.<br/></td>
</tr>
<tr class="even">
<td><strong>HoverEnter</strong></td>
<td>Vários objetos <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de baixa velocidade média.<br/></td>
<td><blockquote>
[!Note]<br />
Pode haver um atraso perceptível antes de receber o gesto do sistema <strong>HoverEnter</strong> . O objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> só receberá esses dados se o objeto <strong>RealTimeStylus</strong> estiver anexado à janela ou ao controle que está diretamente sob a caneta no momento do gesto do sistema.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoverLeave</strong></td>
<td>O objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para o gesto do sistema <strong>HoverEnter</strong> e vários objetos <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de velocidade média suficiente.<br/></td>
<td><blockquote>
[!Note]<br />
Pode haver um atraso perceptível antes de receber o gesto do sistema <strong>HoverLeave</strong> . O objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> só receberá esses dados se o objeto <strong>RealTimeStylus</strong> estiver anexado à janela ou ao controle que está diretamente sob a caneta no momento do gesto do sistema.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="custom-stylus-data"></a>Personalizar dados da caneta

Os dados personalizados da caneta podem ser adicionados ao objeto [**RealTimeStylus**](realtimestylus-class.md) chamando o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) . Os dados personalizados da caneta podem ser adicionados às filas do objeto do **RealTimeStylus** em um dos três locais.

-   Quando o parâmetro *Queue* é definido como **output**, os dados personalizados são adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) após os dados atualmente sendo processados pela coleção de plug-ins síncrona.
-   Quando o parâmetro *Queue* é definido como **OutputImmediate**, os dados personalizados são adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) antes dos dados atualmente sendo processados pela coleção de plug-ins síncrona.
-   Quando o parâmetro de *fila* é definido como **entrada**, os dados personalizados são adicionados à fila de entrada do objeto [**RealTimeStylus**](realtimestylus-class.md) e são enviados para a coleção de plug-ins síncrona antes de novos dados do fluxo de dados da caneta do Tablet.

Em cada um dos casos anteriores, os dados adicionados por plug-ins subsequentes na coleção de plug-in síncrona são adicionados após os dados adicionados pelos plug-ins anteriores.

> [!Note]  
> Se a chamada para o método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) for feita de um plug-in síncrono em resposta a uma chamada para um de seus métodos [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , os dados da caneta personalizada serão adicionados ao fluxo de dados da caneta eletrônica de maneira previsível; caso contrário, ele é adicionado à fila em relação aos dados da caneta atual que o objeto [**RealTimeStylus**](realtimestylus-class.md) está processando e não em relação aos dados que o plug-in assíncrono está processando. O método AddCustomStylusDataToQueue gera uma exceção se o objeto **RealTimeStylus** está desabilitado.

 

Os dados personalizados da caneta são adicionados à fila como um objeto [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) e os plug-ins recebem esses dados por meio de seu método [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. CustomStylusDataAdded](/previous-versions/ms824770(v=msdn.10)) .

Os objetos [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e [**GestureRecognizer**](gesturerecognizer-class.md) podem adicionar dados da caneta personalizada à fila. Para obter mais informações sobre os objetos **DynamicRenderer** e **GestureRecognizer** , consulte plug-ins de [processamento dinâmico](dynamic-renderer-plug-ins.md) e plug- [ins do Recognizer](recognizer-plug-ins.md).

O objeto [**RealTimeStylus**](realtimestylus-class.md) chama o método [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) no thread a partir do qual ele recebe a chamada para seu método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) .

O diagrama a seguir ilustra a adição de dados de caneta personalizada à fila de saída com o parâmetro de *fila* definido como **saída**.

![ilustração mostrando fluxo de dados da caneta personalizada para a fila de saída ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. Os círculos numerados "1", "2" e "3" representam os dados da caneta personalizada que foram adicionados à fila de saída pelo primeiro, segundo e terceiro plug-ins síncronos, respectivamente, em resposta aos dados da caneta eletrônica representados por "C". Os plug-ins adicionaram os dados da caneta personalizada com o parâmetro de *fila* definido como **StylusQueues**. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

O diagrama a seguir ilustra a adição de dados de caneta personalizada à fila de saída com o parâmetro de *fila* definido como **OutputImmediate**.

![Diagrama que mostra o fluxo de dados personalizado da caneta para a fila de saída.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. Os círculos numerados "1", "2" e "3" representam os dados da caneta personalizada que foram adicionados à fila de saída pelo primeiro, segundo e terceiro plug-ins síncronos, respectivamente, em resposta aos dados da caneta eletrônica representados por "C". Os plug-ins adicionaram os dados da caneta personalizada com o parâmetro de *fila* definido como **OutputImmediate**. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

O diagrama a seguir ilustra a adição de dados da caneta personalizada à fila de entrada.

![ilustração mostrando fluxo de dados da caneta personalizada para a fila de saída](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída. Os círculos numerados "1", "2" e "3" representam os dados da caneta personalizada que foram adicionados à fila de entrada pelo primeiro, segundo e terceiro plug-ins síncronos, respectivamente, em resposta aos dados da caneta eletrônica representados por "C". Os plug-ins adicionaram os dados da caneta personalizada com o parâmetro de *fila* definido como **entrada**. Os dados da caneta personalizada numerados "1" são passados para os plug-ins síncronos e, em seguida, para a fila de saída antes dos dados da caneta personalizada numerados "2" e "3", ambos são processados antes que os próximos dados da caneta do Tablet sejam processados. O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

## <a name="error-data"></a>Dados de erro

Quando um plug-in gera uma exceção, o fluxo normal de dados é interrompido. O objeto [**RealTimeStylus**](realtimestylus-class.md) gera um objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) e chama:

-   O método [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) do plug-in que gerou a exceção.
-   O método [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) dos plug-ins restantes nessa coleção.

Se o plug-in que gerou a exceção for um plug-in síncrono, o objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) será adicionado à fila de saída. Em seguida, o objeto [**RealTimeStylus**](realtimestylus-class.md) retoma o processamento normal dos dados originais.

O diagrama a seguir ilustra a adição de dados de erro aos dados da caneta eletrônica.

![fluxo de dados personalizado da caneta para a fila de saída com a adição de dados de erro](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. O círculo "e" representa um objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) gerado pelo objeto **RealTimeStylus** quando o segundo plug-in síncrono, plug-in síncrono 2, gera uma exceção durante o processamento de "C". O objeto **RealTimeStylus** , em seguida, pausa seu processamento de "C" e passa "e" para o plug-in que gerou a exceção e todos os plug-ins subsequentes. O objeto **RealTimeStylus** então coloca "e" na fila de saída e retoma seu processamento de "C", que é passado para os plug-ins restantes na coleção de plug-in síncrona e colocado na fila de saída após "e". O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.

Se um plug-in lançar uma exceção do seu método de erro, o objeto [**RealTimeStylus**](realtimestylus-class.md) capturará a exceção, mas não gerará um novo objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) . Isso é para evitar a recursão.

Os dados de erro são adicionados à fila de saída após qualquer dado da caneta personalizada que é adicionado na posição **OutputImmediate** antes da exceção que criou os dados do erro e antes dos dados da caneta personalizada que são adicionados à posição **OutputImmediate** por plug-ins subsequentes na coleção de plug-in síncrona.

O diagrama a seguir ilustra como os dados de erro são adicionados à fila de saída em relação aos dados personalizados que são adicionados à fila **OutputImmediate** .

![dados de erro adicionados à fila de saída em relação aos dados personalizados adicionados à fila outputimmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

Neste diagrama, os círculos "A" e "B" representam os dados da caneta eletrônica que já foram adicionados à fila de saída do objeto [**RealTimeStylus**](realtimestylus-class.md) e que ainda não foram enviados para a coleção de plug-ins assíncronos. O círculo "C" representa os dados da caneta do Tablet que o objeto **RealTimeStylus** está processando no momento. Os círculos numerados "1", "2" e "3" são adicionados pelo primeiro, segundo e terceiro plug-ins síncronos, respectivamente, à fila **OutputImmediate** em resposta aos dados representados pelo círculo "C". O círculo "e" representa os dados de erro gerados em resposta a uma exceção gerada pelo segundo plug-in após o segundo plug-in adicionar dados personalizados à fila de saída na posição **OutputImmediate** .

Se qualquer plug-in síncrono adicionar dados da caneta personalizada à fila de entrada em resposta aos dados do erro, os dados serão adicionados imediatamente antes dos dados do erro. Se qualquer um dos plug-ins síncronos adicionar dados da caneta personalizada à fila de saída na posição de **saída** em resposta aos dados do erro, os dados serão adicionados imediatamente após os dados do erro.

O objeto [**RealTimeStylus**](realtimestylus-class.md) chama o método [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) no thread do qual a exceção é lançada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Trabalhando com a classe RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
