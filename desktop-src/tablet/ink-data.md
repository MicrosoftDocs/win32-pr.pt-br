---
description: Depois que a tinta é coletada, os aplicativos podem gerenciar, manipular e/ou transferir esses dados para outra mídia.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Dados de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939406"
---
# <a name="ink-data"></a>Dados de tinta

Depois que a tinta é coletada, os aplicativos podem gerenciar, manipular e/ou transferir esses dados para outra mídia. As ações de selecionar, copiar, mover, salvar, exibir e alterar a tinta ocorrem no objeto [**Ink**](inkdisp-class.md) e seus membros [**contidos,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) como a coleção Strokes e os objetos [**Stroke.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

> [!Note]  
> Usando Real-Time caneta, os aplicativos podem optar por manter dados em seu próprio formato (como salvar traços).

 

## <a name="ink-strokes-and-packets"></a>Tinta, traços e pacotes

Um [**objeto Ink**](inkdisp-class.md) é o tipo de dados fundamental que gerencia, manipula e armazena a entrada coletada do objeto [**InkCollector.**](inkcollector-class.md) Um **objeto Ink** contém um ou mais objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) e métodos e propriedades comuns para gerenciar e manipular esses traços. Um traço é definido como o conjunto de dados capturados em uma única sequência de pen-down, pen-move e pen-up. Os dados de traço contêm uma coleção de pacotes. Um pacote é o conjunto de dados que o dispositivo tablet envia em cada ponto de exemplo. Esses dados contêm informações como coordenadas, pressão de caneta, ângulo de caneta e qualquer outra coisa que o hardware possa transmitir. A [**propriedade PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) do **objeto Stroke** descreve os pacotes que um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) gera.

## <a name="strokes"></a>Traços

Você pode obter um instantâneo dos traços em um [**objeto Ink**](inkdisp-class.md) usando a propriedade **Strokes** do objeto [**Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) A **propriedade Strokes** é uma coleção de referências aos traços no objeto **Ink** no momento em que a propriedade **Strokes** é lida. Se os traços são subsequentemente adicionados ou excluídos do objeto **Ink,** uma coleção [**strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) obtida anteriormente não é atualizada. Além disso, a **propriedade Strokes** é um valor e, como qualquer valor, sai do escopo, a menos que seja atribuída a uma variável.

Para manter uma [**propriedade Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) sincronizada com um objeto [**Ink,**](inkdisp-class.md) wrap-a em um manipulador de eventos para os eventos [**StrokesAdded**](inkstrokes-strokesadded.md) e [**StrokesRemoved**](inkstrokes-strokesremoved.md) na coleção [**Strokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) O manipulador deve obter uma nova cópia da propriedade **Strokes** quando um dos eventos é acionado. Tenha cuidado para não adicionar o manipulador de eventos a uma coleção **Strokes** que está fora do escopo antes que o evento seja acionado.

Observe neste exemplo que `theAddedStrokesIDs` é atualizado com uma nova cópia da propriedade strokes no manipulador `StrokesAdded_Event` .


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

A [**propriedade**](inkdisp-class.md) [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) do objeto Ink define o conjunto de informações em cada pacote que o aplicativo obtém de um dispositivo tablet pc. As informações normalmente incluem coordenadas, mas podem incluir informações muito mais detalhadas (dependendo de quais são as funcionalidades do digitalizador de Tablet PC), como pressão de caneta ou ângulo de caneta. Ao definir descrições de pacote no objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) antes de qualquer tinta ser coletada (usando a propriedade DesiredPacketDescription), você tem controle total sobre quais das propriedades de dispositivos tablet pc você deseja receber.

## <a name="extended-properties"></a>Propriedades estendidas

As propriedades estendidas fornecem um mecanismo para anexar dados definidos pelo aplicativo [**ao Ink**](inkdisp-class.md) e a outros objetos. Para obter mais informações sobre propriedades estendidas, consulte a [**coleção ExtendedProperties.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties)

## <a name="ink-rendering"></a>Renderização de tinta

O [**objeto Renderer**](inkrenderer-class.md) é responsável por renderizar [**o Ink.**](inkdisp-class.md) Dado um contexto de tablet apropriado, o objeto **Renderer** pode mapear coordenadas de espaço de tinta para pixels, aplicar transformares de exibição e exibir tinta em telas e impressoras. Os [**métodos Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) e [**DrawStrke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) são os principais métodos para renderizar tinta. Para obter mais informações sobre como exibir tinta em uma janela, consulte o **objeto Renderer.**

## <a name="cusps"></a>Cúspides

Um traço normalmente começa quando a caneta é baixada para a superfície de desenho e termina quando a caneta é elevada. Dentro de um traço, os picos, ângulos e alterações de direção radical são chamados de picos. Os pontos de extremidade de um traço também são considerados desapontos. Por exemplo, a letra maiúscula "L" tem três cumes, um no meio e outro em cada extremidade.

Conforme um traço é inserido, ele normalmente é suavizado e renderizado usando uma curva Bezier (ou polilinha). As curvas de bezier podem transformar os loops em loops pequenos. Por exemplo, o pico da letra cursiva "i" pode ser suavizado para se parecer com o "e" cursivo. Para evitar isso, os renderadores da Microsoft têm uma fase "pre-Bezier" que lida com os recursos de maneira diferente.

Os também podem ser usados para subdividir objetos [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em unidades apagados. Por exemplo, selecionar o lado vertical de um "L" maiústica pode indicar a apagamento apenas desse lado. A parte do traço a ser apagado seria a parte entre dois cumes.

 

 
