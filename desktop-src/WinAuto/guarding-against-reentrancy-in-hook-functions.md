---
title: Proteção contra reentrância em funções de Hook
description: Enquanto uma função de gancho processa um evento, eventos adicionais podem ser disparados, o que pode fazer com que a função de gancho seja reinserida antes que o processamento do evento original seja concluído.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366474"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Proteção contra reentrância em funções de Hook

Enquanto uma função de gancho processa um evento, eventos adicionais podem ser disparados, o que pode fazer com que a função de gancho seja reinserida antes que o processamento do evento original seja concluído. O problema com a reentrância nas funções de Hook é que os eventos são concluídos fora de sequência, a menos que a função de gancho manipule essa situação.

Por exemplo, considere um caso em que uma função de gancho em um programa de leitor de tela está processando o evento [**Event \_ Object \_ VALUECHANGE**](event-constants.md) para um controle de edição. Se, ao processar o primeiro evento de alteração de valor, a função Hook for reinserida para processar um evento de alteração de valor subsequente, o segundo evento será concluído antes do primeiro evento. Essa situação resulta no leitor de tela transmitindo informações imprecisas para o usuário.

Como o processamento de eventos é interrompido, eventos adicionais podem ser recebidos sempre que a função Hook chama uma função que faz com que a fila de mensagens do thread de propriedade seja verificada. Isso acontece quando qualquer um dos seguintes é chamado dentro da função de gancho:

-   A função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)do Windows, [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage), [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea), [**caixa**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)ou [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   O Microsoft Acessibilidade Ativa Functions [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou outro método ou Propriedade Component Object Model (com) que cruza os limites do processo

Como as funções de Hook chamam Propriedades e métodos [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , não é possível evitar a reentrância. A única solução é para os desenvolvedores clientes adicionarem código na função de gancho que detecta a reentrância e tomar a ação apropriada se a função de gancho for reinserida.

 

 