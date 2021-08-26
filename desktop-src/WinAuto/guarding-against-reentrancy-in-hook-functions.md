---
title: Proteção contra reentração em funções de gancho
description: Embora uma função de gancho processe um evento, eventos adicionais podem ser disparados, o que pode fazer com que a função de gancho entre novamente antes que o processamento do evento original seja concluído.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089ac7212823bc64d6c59cdae3d333e96760dfbc25c899cea80071bb39799c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030746"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Proteção contra reentração em funções de gancho

Embora uma função de gancho processe um evento, eventos adicionais podem ser disparados, o que pode fazer com que a função de gancho entre novamente antes que o processamento do evento original seja concluído. O problema com a reentração em funções de gancho é que os eventos são concluídos fora de sequência, a menos que a função de gancho lidar com essa situação.

Por exemplo, considere um caso em que uma função de gancho em um programa de leitor de tela está processando o [**evento EVENT \_ OBJECT \_ VALUECHANGE**](event-constants.md) para um controle de edição. Se, ao processar o primeiro evento de alteração de valor, a função de gancho for reinserido para processar um evento de alteração de valor subsequente, o segundo evento será concluído antes do primeiro evento. Essa situação resulta no leitor de tela transmitindo informações imprecisas para o usuário.

Como o processamento de eventos é interrompido, eventos adicionais podem ser recebidos sempre que a função de gancho chama uma função que faz com que a fila de mensagens do thread de propriedade seja verificada. Isso acontece quando qualquer um dos seguintes são chamados dentro da função de gancho:

-   As Windows [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) [**GetMessage,**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage,**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)ou [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   As Microsoft Active Accessibility funções [**accessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Uma [**interface IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou outro método ou Component Object Model (COM) que cruza os limites do processo

Como as funções de gancho chamam propriedades e métodos [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) e [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) não é possível evitar a reentração. A única solução é que os desenvolvedores cliente adicionem código na função de gancho que detecta reentrância e tome a ação apropriada se a função de gancho for reinserido.

 

 