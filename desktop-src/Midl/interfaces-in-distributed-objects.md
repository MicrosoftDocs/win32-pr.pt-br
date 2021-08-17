---
title: Interfaces em objetos distribuídos
description: Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- MIDL de interfaces, em objetos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8661e7e07f08d35151afe8fb256539ed574b0a0162178e3a9e63dc8c43c59ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807133"
---
# <a name="interfaces-in-distributed-objects"></a>Interfaces em objetos distribuídos

Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos. Em um aplicativo RPC, uma interface especifica:

-   Como os aplicativos cliente e servidor se identificam entre si.
-   Como os dados são transmitidos entre o cliente e o servidor.
-   Procedimentos remotos que o aplicativo cliente pode chamar.
-   Tipos de dados para os parâmetros e valores de retorno dos procedimentos remotos.

O linguagem IDL da Microsoft (MIDL) é para implementar interfaces usadas em aplicativos distribuídos. Com MIDL, um aplicativo pode ter uma interface ou muitos. Cada interface especifica um contrato distribuído exclusivo entre os programas cliente e servidor. Aplicativos baseados em RPC (chamadas de procedimento remoto), Component Object Model (COM) e distribuída Component Object Model (DCOM) especificam suas interfaces usando MIDL.

O MIDL se assemelha a C e C++ de várias maneiras. Para obter uma visão geral da escrita de interfaces MIDL, consulte [desenvolvendo a interface](/windows/desktop/Rpc/developing-the-interface).

 

 