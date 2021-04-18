---
description: O Windows Sockets 1,1 introduziu o mecanismo Async-SELECT para fornecer indicações de eventos de rede que não envolveram a sondagem ou o bloqueio.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Mensagens do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785139"
---
# <a name="windows-messages"></a>Mensagens do Windows

O Windows Sockets 1,1 introduziu o mecanismo Async-SELECT para fornecer indicações de eventos de rede que não envolveram a sondagem ou o bloqueio. A função [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) é usada para registrar um interesse em um ou mais eventos de rede, conforme listado no anterior, e fornecer um identificador de janela a ser usado para notificação. Quando ocorre um evento de rede indicado, uma mensagem do Windows especificada pelo cliente é enviada para a janela indicada. O provedor de serviços deve usar a função [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) para fazer isso.

No Windows, esse pode não ser o mecanismo de notificação mais eficiente e é inconveniente para daemons e serviços que não desejam abrir nenhuma janela. O mecanismo de sinalização de objeto de evento descrito no seguinte é apresentado para resolver esse problema.

 

 
