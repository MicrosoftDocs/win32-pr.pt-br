---
title: Considerações de design para objetos de proxy
description: O design de objeto de proxy e acessível depende do design dos elementos de interface do usuário do servidor. Independentemente do design, um elemento de interface do usuário deve notificar seu objeto proxy logo antes que ele seja destruído para que o objeto proxy manipule chamadas de clientes adequadamente.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005106"
---
# <a name="design-considerations-for-proxy-objects"></a>Considerações de design para objetos de proxy

O design de objeto de proxy e acessível depende do design dos elementos de interface do usuário do servidor. Independentemente do design, um elemento de interface do usuário deve notificar seu objeto proxy logo antes que ele seja destruído para que o objeto proxy manipule chamadas de clientes adequadamente.

A lista a seguir descreve duas possibilidades de design:

-   Coloque o código que implementa a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no mesmo módulo que o código que implementa o elemento de interface do usuário se o código da interface do usuário for facilmente extensível. Nesse caso, o proxy é "leve" no sentido de que tudo o que ele faz é monitorar o período de vida do objeto acessível, encaminhar chamadas para o objeto acessível e retornar os resultados.
-   Coloque o código que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no mesmo módulo que o código que implementa o objeto proxy. Nesse caso, o objeto acessível usa funções internas para obter informações sobre o elemento de interface do usuário.

## <a name="trackbar-controls"></a>Controles TrackBar

Ao implementar controles TrackBar, use o estilo TrackBar **TBS \_ invertido** para fornecer informações mais significativas. Esse estilo inverte a escala usada por [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

Para trackbars verticais sem esse estilo, [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retorna zero (0) quando o TrackBar Thumb está na parte superior do controle; os valores aumentam à medida que você desliza o polegar para a parte inferior. Com o **estilo \_ revertido TBS** , **IAccessible:: get \_ accValue** retorna 100 (100) quando o TrackBar Thumb está na parte superior; os números diminuem à medida que você move o TrackBar Thumb para a parte inferior.

Para trackbars horizontais sem esse estilo, zero (0) é retornado quando o TrackBar Thumb está na extremidade esquerda do controle; os valores aumentam à medida que você move o TrackBar Thumb para a direita. Com o **estilo \_ revertido TBS** , [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retorna 100 (100) quando o TrackBar Thumb está à esquerda; os valores diminuem à medida que você move o TrackBar Thumb para a direita.

 

 




