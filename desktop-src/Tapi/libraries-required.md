---
description: A seguir está uma lista de arquivos. lib necessários para compilar vários aplicativos TAPI 3, a partir de 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliotecas necessárias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621356"
---
# <a name="libraries-required"></a>Bibliotecas necessárias

Uma lista de arquivos. lib necessários para compilar vários aplicativos TAPI 3, a partir de 1/22/01:

-   Advapi32. lib
-   Amstrmid. lib (os GUIDs do ActiveMovie)
-   Kernel32.lib
-   Mdhcpid. lib (GUIDs multicast)
-   Ole32. lib (COM)
-   Oleaut32. lib (automação COM)
-   Rendid. lib (GUIDs de reunião)
-   Rpcndr. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Sdpblbid. lib (os GUIDs do SDP (Session Descriptor Protocol))
-   Strmiids. lib
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   Ws2 \_ 32. lib

se você estiver usando Microsoft Visual Studio, talvez seja necessário atualizar sua versão. Em particular, Link.exe deve conter uma data de 3/19/98 ou posterior.

O compilador define deve incluir \_ Win32 \_ WinNT definido como pelo menos 0x500 e \_ Win32 \_ DCOM.

 

 



