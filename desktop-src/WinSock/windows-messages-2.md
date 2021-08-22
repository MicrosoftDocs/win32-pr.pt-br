---
description: Windows Os soquetes 1.1 introduziram o mecanismo assíncrono de seleção para fornecer indicações de evento de rede que não envolveram sondagem ou bloqueio.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows Mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bab33ecb4d2898c8f1e363ab19ad425503e9d005bf24229a29f581aadf1788f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993206"
---
# <a name="windows-messages"></a>Windows Mensagens

Windows Os soquetes 1.1 introduziram o mecanismo assíncrono de seleção para fornecer indicações de evento de rede que não envolveram sondagem ou bloqueio. A [**função WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) é usada para registrar um interesse em um ou mais eventos de rede, conforme listado no anterior, e fornecer um alça de janela a ser usado para notificação. Quando ocorre um evento de rede nomeado, uma mensagem de Windows especificada pelo cliente é enviada para a janela indicada. O provedor de serviços deve usar [**a função WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) para fazer isso.

No Windows, esse pode não ser o mecanismo de notificação mais eficiente e é inconveniente para daemons e serviços que não querem abrir janelas. O mecanismo de sinalização de objeto de evento descrito no seguinte é introduzido para resolver esse problema.

 

 
