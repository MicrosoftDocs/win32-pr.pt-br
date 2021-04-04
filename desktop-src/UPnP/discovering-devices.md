---
title: Descobrindo dispositivos
description: Você pode pesquisar dispositivos de três maneiras por tipo, por UDN, e pela pesquisa assíncrona (que é uma pesquisa por tipo de dispositivo).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055d08db76edd5bcc5591d3254613462c00fc974
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822935"
---
# <a name="discovering-devices"></a>Descobrindo dispositivos

Você pode pesquisar dispositivos de três maneiras: por tipo, por UDN e pela pesquisa assíncrona (que é uma pesquisa por tipo de dispositivo).

![janela descobrir dispositivos](images/ucp-disc.png)

**Para descobrir dispositivos**

1.  Selecione o tipo de pesquisa que você deseja usar: **Localizar por tipo**, **Localizar por UDN** ou **localização assíncrona**.
2.  Selecione o tipo de dispositivo ou o UDN que você deseja localizar na lista (para pesquisas por tipo ou por UDN). O conteúdo da lista é baseado no conteúdo do udn.txt e devtype.txt arquivos que você editou anteriormente.
3.  Clique em **Iniciar Descoberta**. A pesquisa é iniciada. Os resultados são exibidos na lista **dispositivos encontrados** . Se nenhum dispositivo for encontrado, será exibida uma mensagem indicando essa condição. O status do progresso da pesquisa é exibido no campo **status** .

Quando você usa a pesquisa assíncrona, novos dispositivos que são encontrados são exibidos na lista **dispositivos encontrados** e na barra de **status** . Quando a pesquisa assíncrona for concluída, a barra de **status** exibirá uma mensagem indicando isso. No entanto, como uma pesquisa assíncrona é executada até ser interrompida manualmente, novos dispositivos aparecem na lista **dispositivos encontrados** e a barra de **status** como os dispositivos aparecem na rede.

Depois de descobrir os dispositivos, você pode [controlá-los](controlling-a-device.md).

 

 




