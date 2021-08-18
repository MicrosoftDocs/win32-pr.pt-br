---
title: Parâmetro de preferência de teclado
description: O parâmetro de preferência do teclado indica que o usuário depende do teclado em vez do mouse, portanto, os aplicativos devem exibir interfaces de teclado que, de outra forma, seriam ocultas.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c074078cdd548b6b3614213d6086edb3f5a6a412d84e418417dc0b4fcd2800e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998476"
---
# <a name="keyboard-preference-parameter"></a>Parâmetro de preferência de teclado

O parâmetro de preferência do teclado indica que o usuário depende do teclado em vez do mouse, portanto, os aplicativos devem exibir interfaces de teclado que, de outra forma, seriam ocultas.

O usuário controla a configuração do parâmetro de preferência do teclado usando o Central de Facilidade de Acesso no Painel de Controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os sinalizadores **\_ SPI GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de preferência do teclado.

Além disso, no Windows 2000, os usuários podem definir um parâmetro que indica se as chaves de acesso de menu são sempre sublinhadas. Os aplicativos usam os sinalizadores **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de sublinhados do menu.

Quando um aplicativo recebe uma mensagem [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) para a preferência do teclado ou o parâmetro de sublinhado do menu, é recomendável que o aplicativo chame [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para atualizar as informações de ambos os parâmetros.

Observe que **SPI \_ GETMENUUNDERLINES** é o mesmo **que SPI \_ GETKEYBOARDCUES** e **SPI \_ SETMENUUNDERLINES** é o mesmo **que SPI \_ SETKEYBOARDCUES**.

 

 