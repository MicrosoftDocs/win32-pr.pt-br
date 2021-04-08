---
description: O destino padrão pode ser alterado simplesmente chamando WSPConnect novamente, mesmo que o soquete já esteja conectado. Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Reconectando e desconectando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827851"
---
# <a name="reconnecting-and-disconnecting"></a>Reconectando e desconectando

O destino padrão pode ser alterado simplesmente chamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) novamente, mesmo que o soquete já esteja conectado. Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um **WSPConnect** anterior.

Se o endereço fornecido para o soquete for todos os zeros, o Soquete será desconectado – o endereço remoto padrão será indeterminado, portanto chamadas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) retornarão o código de erro WSAENOTCONN, embora [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) ainda possam ser usados.

 

 
