---
description: A seguir está uma lista de arquivos. lib necessários para compilar vários aplicativos TAPI 3, a partir de 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliotecas necessárias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779457"
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

Se você estiver usando Microsoft Visual Studio, talvez seja necessário atualizar sua versão. Em particular, Link.exe deve conter uma data de 3/19/98 ou posterior.

O compilador define deve incluir \_ Win32 \_ WinNT definido como pelo menos 0x500 e \_ Win32 \_ DCOM.

 

 



