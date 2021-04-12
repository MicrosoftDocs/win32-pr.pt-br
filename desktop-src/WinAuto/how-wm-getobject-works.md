---
title: Como WM_GETOBJECT funciona
description: O Microsoft Acessibilidade Ativa envia a \_ mensagem do WM GetObject para o aplicativo de servidor apropriado quando um cliente chama uma das funções AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe287bca68c925cb7be95ff52d2dac547ed097
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294109"
---
# <a name="how-wm_getobject-works"></a>Como o WM \_ GetObject funciona

O Microsoft Acessibilidade Ativa envia a mensagem do [**WM \_ GetObject**](wm-getobject.md) para o aplicativo de servidor apropriado quando um cliente chama uma das funções **AccessibleObjectFrom * * * X* . A lista a seguir descreve os vários cenários que ocorrem:

-   Se a janela ou o controle que recebe o [**WM \_ GetObject**](wm-getobject.md) implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), a janela retornará uma referência à interface **IAccessible** usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). O Microsoft Acessibilidade Ativa, em conjunto com a biblioteca do Component Object Model (COM), executa o marshaling apropriado e passa o ponteiro de interface do servidor de volta para o cliente.
-   Se a janela que recebe a mensagem não implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), ela deverá retornar zero.
-   Se a janela não tratar a mensagem do [**WM \_ GetObject**](wm-getobject.md) , a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retornará zero.

Mesmo se o servidor retornar zero, o Microsoft Acessibilidade Ativa ainda fornecerá ao cliente informações sobre o objeto. Para a maioria dos objetos fornecidos pelo sistema, como caixas de listagem e botões, o Microsoft Acessibilidade Ativa fornece informações completas; para outros objetos, as informações são limitadas. Por exemplo, o Microsoft Acessibilidade Ativa não fornece informações para controles que não têm um identificador de janela. O Microsoft Acessibilidade Ativa retorna um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com proxy que o cliente usa para obter informações sobre o objeto.

Para obter mais informações, consulte [a \_ mensagem do WM GetObject](the-wm-getobject-message.md).

 

 