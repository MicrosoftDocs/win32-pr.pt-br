---
description: Fornece acesso aos eventos da caneta provenientes de digitalizadores de caneta ou de toque.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referência do RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170461"
---
# <a name="realtimestylus-reference"></a>Referência do RealTimeStylus

Fornece acesso aos eventos da caneta provenientes de digitalizadores de caneta ou de toque.

## <a name="in-this-section"></a>Nesta seção

-   [Interfaces e classes do RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumerações do RealTimeStylus](realtimestylus-enumerations.md)
-   [Estruturas RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Comentários

Esse objeto implementa a interface com do [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Você pode controlar totalmente, dinamicamente renderizar, modificar e até mesmo excluir dados do fluxo de pacotes dentro dos plug-ins síncronos e assíncronos do objeto de [**classe RealTimeStylus**](realtimestylus-class.md) .

A caneta em tempo real fornece uma maneira de criar um objeto **InkCollecting** que é de thread único e residente no thread de interface do usuário do aplicativo. Esse objeto **InkCollecting** acessa os dados da caneta em tempo real da fila. Um objeto **InkCollecting** em conjunto com a caneta em tempo real permite a edição de seleção em tempo real e a edição em tempo real dos dados de tinta coletados. Para obter mais informações, consulte [acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md).

Use o objeto da [**classe RealTimeStylus**](realtimestylus-class.md) para interagir diretamente com o fluxo de dados da caneta do Tablet ou para bloquear a escrita em tempo real. Use o controle de controle de [**classe InkCollector**](inkcollector-class.md) , objeto de [**classe InkOverlay**](inkoverlay-class.md) , controle de controle [InkPicture](inkpicture-control-reference.md) ou [InkEdit](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornecer o comportamento de que você precisa.

Os eventos de caneta em tempo real estão em um identificador de janela específico dentro de um retângulo de entrada de janela específico. O RealTimeStylusService pode enviar dados de caneta para vários objetos de [**classe RealTimeStylus**](realtimestylus-class.md) . Cada objeto da **classe RealTimeStylus** recebe dados da caneta para uma seção específica de uma janela com base na [**Propriedade IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para esse objeto de **classe do RealTimeStylus** . O objeto da **classe RealTimeStylus** Obtém os dados da caneta e, em seguida, processa isso por meio de uma lista de plug-ins síncronos e assíncronos.

A diferença entre os plug-ins síncronos e os plug-ins assíncronos está no thread em que eles são executados e na sequência de chamada. Plug-ins síncronos são chamados pelo thread no qual o objeto de [**classe RealTimeStylus**](realtimestylus-class.md) é executado. Toda vez que o objeto de **classe RealTimeStylus** é instanciado, um thread de execução é instanciado. Plug-ins síncronos são executados neste novo thread instanciado para a instância do objeto de **classe RealTimeStylus** . Plug-ins assíncronos são chamados por meio da interface do usuário ou do thread do aplicativo após o fluxo do pacote ter sido processado pelos plug-ins síncronos e armazenados na fila de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
