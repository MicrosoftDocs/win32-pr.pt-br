---
title: Interfaces em objetos distribuídos
description: Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- MIDL de interfaces, em objetos distribuídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294012"
---
# <a name="interfaces-in-distributed-objects"></a>Interfaces em objetos distribuídos

Na computação distribuída, uma interface é uma coleção de definições e funções remotas que permite que dois ou mais programas interoperem entre diferentes contextos. Em um aplicativo RPC, uma interface especifica:

-   Como os aplicativos cliente e servidor se identificam entre si.
-   Como os dados são transmitidos entre o cliente e o servidor.
-   Procedimentos remotos que o aplicativo cliente pode chamar.
-   Tipos de dados para os parâmetros e valores de retorno dos procedimentos remotos.

O linguagem IDL da Microsoft (MIDL) é para implementar interfaces usadas em aplicativos distribuídos. Com MIDL, um aplicativo pode ter uma interface ou muitos. Cada interface especifica um contrato distribuído exclusivo entre os programas cliente e servidor. Aplicativos baseados em RPC (chamadas de procedimento remoto), Component Object Model (COM) e distribuída Component Object Model (DCOM) especificam suas interfaces usando MIDL.

O MIDL se assemelha a C e C++ de várias maneiras. Para obter uma visão geral da escrita de interfaces MIDL, consulte [desenvolvendo a interface](/windows/desktop/Rpc/developing-the-interface).

 

 