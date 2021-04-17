---
description: A noção de bloqueio em um ambiente do Windows tem sido historicamente muito importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763520"
---
# <a name="blocking-operations"></a>Operações de bloqueio

A noção de bloqueio em um ambiente do Windows tem sido historicamente muito importante. Nos ambientes do Windows Sockets 1,1, as chamadas de bloqueio foram desencorajadas, pois elas tendiamm para desabilitar a interação contínua com o sistema. Além disso, eles empregam uma técnica pseudoblocking, que, por vários motivos, nem sempre funciona conforme o esperado. No entanto, em ambientes Windows programados de forma preventiva, as chamadas de bloqueio fazem muito mais sentido, podem ser implementadas por serviços do sistema operacional nativo e, na verdade, são um mecanismo preferencial. A API do Winsock 2 não dá mais suporte a psuedoblocking, mas como os shims de compatibilidade do Windows Sockets 1,1 devem continuar emulando esse comportamento, os provedores de serviços devem dar suporte a isso, conforme descrito a seguir.

 

 



