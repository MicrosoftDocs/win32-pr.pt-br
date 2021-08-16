---
description: a noção de bloqueio em um ambiente de Windows tem sido historicamente muito importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322431"
---
# <a name="blocking-operations"></a>Operações de bloqueio

a noção de bloqueio em um ambiente de Windows tem sido historicamente muito importante. nos ambientes do Windows sockets 1,1, as chamadas de bloqueio foram desencorajadas, pois elas tendiamm para desabilitar a interação contínua com o sistema. Além disso, eles empregam uma técnica pseudoblocking, que, por vários motivos, nem sempre funciona conforme o esperado. no entanto, em ambientes de Windows programados de forma preventiva, as chamadas de bloqueio fazem muito mais sentido, podem ser implementadas pelos serviços nativos do sistema operacional e, na verdade, são um mecanismo preferencial. a API do Winsock 2 não dá mais suporte a psuedoblocking, mas como os shims de compatibilidade do Windows sockets 1,1 devem continuar emulando esse comportamento, os provedores de serviços devem dar suporte a isso, conforme descrito a seguir.

 

 



