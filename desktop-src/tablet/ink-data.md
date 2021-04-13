---
description: Depois que a tinta é coletada, os aplicativos podem gerenciar, manipular e/ou transferir esses dados para outras mídias.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Dados de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de73291269398ae42a47ee26897c8da9bac8abe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501626"
---
# <a name="ink-data"></a>Dados de tinta

Depois que a tinta é coletada, os aplicativos podem gerenciar, manipular e/ou transferir esses dados para outras mídias. As ações de selecionar, copiar, mover, salvar, exibir e alterar a tinta ocorrem no objeto de [**tinta**](inkdisp-class.md) e seus membros independentes, como a coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

> [!Note]  
> Usando a caneta Real-Time, os aplicativos podem optar por manter os dados em seu próprio formato (como salvar traços).

 

## <a name="ink-strokes-and-packets"></a>Tinta, traços e pacotes

Um objeto [**Ink**](inkdisp-class.md) é o tipo de dados fundamental que gerencia, manipula e armazena a entrada coletada do objeto [**InkCollector**](inkcollector-class.md) . Um objeto **Ink** contém um ou mais objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) e propriedades e métodos comuns para gerenciar e manipular esses traços. Um traço é definido como o conjunto de dados que é capturado em uma única sequência de caneta para baixo, movimento de caneta e para a caneta. Os dados de traço contêm uma coleção de pacotes. Um pacote é o conjunto de dados que o dispositivo do Tablet envia em cada ponto de amostra. Esses dados contêm informações como coordenadas, pressão da caneta, ângulo da caneta e qualquer outra coisa que o hardware possa transmitir. A propriedade [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) do objeto **Stroke** descreve os pacotes que um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) gera.

## <a name="strokes"></a>Traços

Você pode obter um instantâneo dos traços em um objeto de [**tinta**](inkdisp-class.md) usando a propriedade [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) do objeto de **tinta** . A propriedade **Strokes** é uma coleção de referências aos traços no objeto **Ink** no momento em que a propriedade **Strokes** é lida. Se os traços forem adicionados ou excluídos posteriormente do objeto de **tinta** , uma coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) obtida anteriormente não será atualizada. Além disso, a propriedade **Strokes** é um valor e, como qualquer valor, sai do escopo, a menos que seja atribuída a uma variável.

Para manter uma propriedade [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) sincronizada com um objeto [**Ink**](inkdisp-class.md) , empacote-a em um manipulador de eventos para os eventos [**StrokesAdded**](inkstrokes-strokesadded.md) e [**StrokesRemoved**](inkstrokes-strokesremoved.md) na coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . O manipulador deve obter uma nova cópia da propriedade **Strokes** quando um dos eventos é acionado. Tenha cuidado para não adicionar o manipulador de eventos a uma coleção de **traços** fora do escopo antes de o evento ser acionado.

Observe neste exemplo que `theAddedStrokesIDs` é atualizado com uma nova cópia da Propriedade Strokes no `StrokesAdded_Event` manipulador.


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>Propriedade PacketDescription

A propriedade [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) do objeto de [**tinta**](inkdisp-class.md) define o conjunto de informações em cada pacote que o aplicativo obtém de um dispositivo de Tablet PC. As informações normalmente incluem coordenadas, mas podem incluir informações muito mais detalhadas (dependendo dos recursos do digitalizador do Tablet PC), como pressão da caneta ou ângulo da caneta. Ao definir descrições de pacote no objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) antes que qualquer tinta seja coletada (usando a Propriedade DesiredPacketDescription), você tem controle total sobre quais das propriedades de dispositivos do Tablet PC você deseja receber.

## <a name="extended-properties"></a>Propriedades estendidas

As propriedades estendidas fornecem um mecanismo para anexar dados definidos pelo aplicativo à [**tinta**](inkdisp-class.md) e a outros objetos. Para obter mais informações sobre propriedades estendidas, consulte a coleção [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) .

## <a name="ink-rendering"></a>Renderização de tinta

O objeto de [**processador**](inkrenderer-class.md) é responsável por renderizar a [**tinta**](inkdisp-class.md). Dado um contexto de Tablet apropriado, o objeto de **processador** pode mapear coordenadas de espaço de tinta para pixels, aplicar transformações de exibição e exibir tinta em telas e impressoras. Os métodos [**draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) e [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) são os principais métodos para renderização de tinta. Para obter mais informações sobre como exibir tinta em uma janela, consulte o objeto **Renderer** .

## <a name="cusps"></a>Cusps

Um traço normalmente começa quando a caneta é diminuída para a superfície de desenho e termina quando a caneta é gerada. Dentro de um traço, os picos, ângulos e alterações de ângulo são chamados de cusps. Os pontos de extremidade de um traço também são considerados cusps. Por exemplo, a letra maiúscula "L" tem três cusps, uma no meio e uma em cada extremidade.

Como um traço é inserido, ele é normalmente suave e renderizado usando uma curva de Bezier (ou polilinha). As curvas de Bézier podem transformar cusps em loops pequenos. Por exemplo, o pico da letra cursiva "i" pode ser suavizado para se parecer com o "e" cursivo. Para evitar isso, os renderizadores da Microsoft têm uma fase de "pré-Bézier" que manipula o cusps de forma diferente.

Cusps também pode ser usado para subdividir objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em unidades apagáveis. Por exemplo, selecionar o lado vertical de um "L" maiúsculo pode indicar apagar apenas esse lado. A parte do traço a ser apagado seria a parte entre dois cusps.

 

 
