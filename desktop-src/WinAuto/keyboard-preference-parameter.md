---
title: Parâmetro de preferência de teclado
description: O parâmetro de preferência de teclado indica que o usuário depende do teclado, em vez do mouse, de modo que os aplicativos devem exibir as interfaces de teclado que, de outra forma, seriam ocultas.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366260"
---
# <a name="keyboard-preference-parameter"></a>Parâmetro de preferência de teclado

O parâmetro de preferência de teclado indica que o usuário depende do teclado, em vez do mouse, de modo que os aplicativos devem exibir as interfaces de teclado que, de outra forma, seriam ocultas.

O usuário controla a configuração do parâmetro de preferência de teclado usando a central de facilidade de acesso no painel de controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os sinalizadores **SPI \_ GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de preferência de teclado.

Além disso, no Windows 2000, os usuários podem definir um parâmetro que indica se as teclas de acesso do menu sempre serão sublinhadas. Os aplicativos usam os sinalizadores **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro sublinhado do menu.

Quando um aplicativo recebe uma mensagem de [**\_ SETTINGCHANGE do WM**](/windows/desktop/winmsg/wm-settingchange) para o parâmetro de sublinhado de menu ou de preferência de teclado, é recomendável que o aplicativo chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para atualizar as informações para ambos os parâmetros.

Observe que **o \_ SPI GETMENUUNDERLINES** é o mesmo que **SPI \_ GETKEYBOARDCUES**, e **SPI \_ SETMENUUNDERLINES** é o mesmo que **SPI \_ SETKEYBOARDCUES**.

 

 