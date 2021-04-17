---
description: WSPConnect estabelece um endereço de destino padrão para habilitar um soquete a ser usado com as operações Send (WSPSend) e Receive (WSPRecv) subsequentes.
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Conectando-se a um par padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763198"
---
# <a name="connecting-to-a-default-peer"></a>Conectando-se a um par padrão

Para um soquete associado a um protocolo sem conexão, a operação executada pelo [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) é simplesmente para estabelecer um endereço de destino padrão para que o soquete possa ser usado com as operações de envio e recepção subsequentes ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))). Todos os datagramas recebidos de um endereço diferente do endereço de destino especificado serão descartados.

 

 
