---
description: Há sete pincéis de ações lógicas predefinidos mantidos pela interface gráfica do dispositivo (GDI). Também há 21 pincéis de estoque lógicos predefinidos mantidos pela interface de gerenciamento do Windows (usuário).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pincel de ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968144"
---
# <a name="stock-brush"></a>Pincel de ações

Há sete pincéis de ações lógicas predefinidos mantidos pela interface gráfica do dispositivo (GDI). Também há 21 pincéis de estoque lógicos predefinidos mantidos pela interface de gerenciamento do Windows (usuário).

A ilustração a seguir mostra retângulos pintados usando os sete pincéis de ações predefinidos.

![ilustração mostrando sete caixas: uma preta, três tons de cinza e três que aparecem vazias](images/csbru-03.png)

Um aplicativo pode recuperar um identificador que identifica um dos sete pincéis de ações chamando a função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , especificando o tipo de pincel.

Os 21 pincéis de estoque mantidos pela interface de gerenciamento do Windows correspondem às cores dos elementos da janela, como menus, barras de rolagem e botões. Um aplicativo pode obter um identificador que identifica um desses pincéis chamando a função [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) e especificando um valor de cor do sistema. Um aplicativo pode recuperar a cor correspondente a um determinado elemento de janela chamando a função [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) . Um aplicativo pode definir a cor correspondente a um elemento de janela chamando a função [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .

 

 
