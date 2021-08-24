---
title: Como WM_GETOBJECT funciona
description: Microsoft Active Accessibility envia a mensagem WM GETOBJECT para o aplicativo de servidor apropriado quando um cliente chama uma das funções \_ AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795756"
---
# <a name="how-wm_getobject-works"></a>Como o WM \_ GETOBJECT funciona

Microsoft Active Accessibility envia a [**mensagem WM \_ GETOBJECT para**](wm-getobject.md) o aplicativo de servidor apropriado quando um cliente chama uma das funções **AccessibleObjectFrom**_X._ A lista a seguir descreve os vários cenários que ocorrem:

-   Se a janela ou controle que recebe [**WM \_ GETOBJECT**](wm-getobject.md) implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), a janela retornará uma referência à interface **IAccessible** usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, em conjunto com a biblioteca Component Object Model (COM), executa o marshaling apropriado e passa o ponteiro de interface do servidor de volta para o cliente.
-   Se a janela que recebe a mensagem não implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), ela deverá retornar zero.
-   Se a janela não tratar a [**mensagem WM \_ GETOBJECT,**](wm-getobject.md) a [função DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retornará zero.

Mesmo que o servidor retorne zero, Microsoft Active Accessibility ainda fornece ao cliente informações sobre o objeto . Para a maioria dos objetos fornecidos pelo sistema, como caixas de listagem e botões, Microsoft Active Accessibility fornece informações completas; para outros objetos, as informações são limitadas. Por exemplo, Microsoft Active Accessibility fornece informações para controles que não têm um alça de janela. Microsoft Active Accessibility retorna um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que o cliente usa para obter informações sobre o objeto.

Para obter mais informações, [consulte A mensagem \_ GETOBJECT do WM.](the-wm-getobject-message.md)

 

 