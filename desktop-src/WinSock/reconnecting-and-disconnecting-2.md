---
description: O destino padrão pode ser alterado simplesmente chamando WSPConnect novamente, mesmo que o soquete já esteja conectado. Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Reconectando e desconectando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4c50872b6690c42d97c3696bcfcb2586b9b5b510c17aafc5dcc159b17ed56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121356"
---
# <a name="reconnecting-and-disconnecting"></a>Reconectando e desconectando

O destino padrão pode ser alterado simplesmente chamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) novamente, mesmo que o soquete já esteja conectado. Os datagrams enfileirados para recebimento serão descartados se o novo endereço for diferente do endereço especificado em um **WSPConnect** anterior.

Se o endereço fornecido para o soquete for todos os zeros, o Soquete será desconectado – o endereço remoto padrão será indeterminado, portanto chamadas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) retornarão o código de erro WSAENOTCONN, embora [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) ainda possam ser usados.

 

 
