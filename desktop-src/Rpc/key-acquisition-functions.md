---
title: Funções de aquisição de chave
description: Por padrão, o SSP fornece chaves de criptografia para programas de servidor que as solicitam. Cada SSP implementa seu próprio sistema de geração de chaves. O formato das chaves que o SSP gera é específico para o SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020228"
---
# <a name="key-acquisition-functions"></a>Funções de aquisição de chave

Por padrão, o SSP fornece chaves de criptografia para programas de servidor que as solicitam. Cada SSP implementa seu próprio sistema de geração de chaves. O formato das chaves que o SSP gera é específico para o SSP.

O RPC fornece a capacidade de substituir o método padrão de geração de chaves de criptografia. Seu aplicativo pode chamar a [**função RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passar um ponteiro para uma função de aquisição de chave. Você pode escrever a função de aquisição de chave para que ela gere chaves usando qualquer método escolhido. No entanto, a chave que ele passa para o programa de servidor deve corresponder ao formato que o SSP requer.

> [!Note]  
> A maioria dos aplicativos não precisa usar funções de aquisição de chaves e pode simplesmente fornecer **NULL** para todos os parâmetros em que uma função de aquisição de chave é solicitada.

 

 

 




