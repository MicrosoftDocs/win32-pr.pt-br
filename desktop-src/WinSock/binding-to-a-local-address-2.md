---
description: Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa ser vinculado a um endereço local.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Associação a um endereço local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132749"
---
# <a name="binding-to-a-local-address"></a>Associação a um endereço local

Antes que um soquete possa ser usado para configurar uma conexão ou receber uma solicitação de conexão, ele precisa ser vinculado a um endereço local. Isso pode ser feito explicitamente chamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))ou implicitamente pelo [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se o soquete não estiver conectado quando essa função for chamada.

 

 
