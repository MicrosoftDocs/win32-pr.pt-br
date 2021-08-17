---
description: Fornece acesso aos eventos de caneta provenientes de digitalizadores de caneta ou toque.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referência de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05518658a7bca01090e72cbe68d23b98d5ffffed14b2d8d091fa8c884e9f7c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091456"
---
# <a name="realtimestylus-reference"></a>Referência de RealTimeStylus

Fornece acesso aos eventos de caneta provenientes de digitalizadores de caneta ou toque.

## <a name="in-this-section"></a>Nesta seção

-   [Interfaces e classes RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumerações RealTimeStylus](realtimestylus-enumerations.md)
-   [Estruturas RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Comentários

Esse objeto implementa a interface [**COM IRealTimeStylus.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)

Esse objeto pode ser instanado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Você pode controlar totalmente, renderizar, modificar e até mesmo excluir dados do fluxo de pacotes dentro dos plug-ins síncronos e assíncronos do objeto [**classe RealTimeStylus.**](realtimestylus-class.md)

A caneta em tempo real fornece uma maneira de criar um objeto **InkCollecting** que é de thread único e residente no thread da interface do usuário do aplicativo. Esse **objeto InkCollecting** acessa os dados da caneta em tempo real da fila. Um **objeto InkCollecting** em conjunto com a caneta em tempo real permite a edição de seleção em tempo real e a edição em tempo real dos dados de tinta coletados. Para obter mais informações, consulte [Acessando e manipulando a](accessing-and-manipulating-stylus-input.md)entrada da caneta.

Use o [**objeto Classe RealTimeStylus**](realtimestylus-class.md) para interagir diretamente com o fluxo de dados da caneta do tablet ou para bloquear a inking em tempo real. Use o [**objeto Classe InkCollector,**](inkcollector-class.md) o objeto [**Classe InkOverlay,**](inkoverlay-class.md) o controle [InkPicture Control](inkpicture-control-reference.md) ou o controle [InkEdit Control](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornece o comportamento necessário.

Os eventos de caneta em tempo real estão em um alça de janela específico dentro de um retângulo de entrada de janela específico. O RealTimeStylusService pode enviar dados de caneta para vários [**objetos da Classe RealTimeStylus.**](realtimestylus-class.md) Cada objeto da Classe **RealTimeStylus** recebe dados de caneta para uma seção específica de uma janela com base na propriedade [**IRealTimeStylus::WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para esse objeto **classe RealTimeStylus.** O **objeto Classe RealTimeStylus** obtém os dados da caneta e, em seguida, processa isso por meio de uma lista de plug-ins síncronos e assíncronos.

A diferença entre os plug-ins síncronos e os plug-ins assíncronos está no thread no qual eles são executados e na sequência de chamada. Plug-ins síncronos são chamados pelo thread no qual o objeto [**Classe RealTimeStylus**](realtimestylus-class.md) é executado. Sempre que **o objeto Classe RealTimeStylus** é instautado, um thread de execução é instariado. Plug-ins síncronos são executados nesse novo thread instanciado para a instância do objeto **Classe RealTimeStylus.** Plug-ins assíncronos são chamados por meio da interface do usuário ou do thread do aplicativo depois que o fluxo de pacotes é processado pelos plug-ins síncronos e armazenados na fila de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**Istylussyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**Istylusasyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
