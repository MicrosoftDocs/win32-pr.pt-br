---
title: Como dar suporte a itens de retorno de chamada
description: Este tópico demonstra como fornecer suporte para itens de retorno de chamada.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917791"
---
# <a name="how-to-support-callback-items"></a>Como dar suporte a itens de retorno de chamada

Este tópico demonstra como fornecer suporte para itens de retorno de chamada.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Se seu aplicativo for usar itens de retorno de chamada em um controle ComboBoxEx, ele deverá estar preparado para lidar com o código de notificação [ \_ GETDISPINFO do CBEN](cben-getdispinfo.md) . Um controle ComboBoxEx envia essa notificação sempre que precisa do proprietário para fornecer informações de item específicas. Para obter mais informações sobre itens de retorno de chamada, consulte [itens de retorno de chamada](comboboxex-controls.md).

A função definida pelo aplicativo a seguir processa [CBEN \_ GETDISPINFO](cben-getdispinfo.md) fornecendo atributos para um determinado item. Observe que ele define o membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de entrada para CBEIF \_ di \_ SETITEM. A definição de **Mask** para esse valor faz com que o controle retenha as informações do item para que não seja necessário solicitar as informações novamente.

## <a name="complete-example"></a>Exemplo completo


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referência de controle ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usando controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 