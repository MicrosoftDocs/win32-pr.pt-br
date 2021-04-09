---
title: Funções de aquisição de chave
description: Por padrão, o SSP fornece chaves de criptografia para programas de servidor que os solicitam. Cada SSP implementa seu próprio sistema de geração de chaves. O formato das chaves que o SSP gera são específicos para o SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822933"
---
# <a name="key-acquisition-functions"></a>Funções de aquisição de chave

Por padrão, o SSP fornece chaves de criptografia para programas de servidor que os solicitam. Cada SSP implementa seu próprio sistema de geração de chaves. O formato das chaves que o SSP gera são específicos para o SSP.

O RPC fornece a capacidade de substituir o método padrão de geração de chaves de criptografia. Seu aplicativo pode chamar a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) e passá-la para um ponteiro para uma função de aquisição de chave. Você pode escrever a função de aquisição de chave para que ela gere chaves usando qualquer método escolhido. No entanto, a chave que ele passa para o programa do servidor deve corresponder ao formato exigido pelo SSP.

> [!Note]  
> A maioria dos aplicativos não precisa usar as principais funções de aquisição e pode simplesmente fornecer **NULL** a todos os parâmetros em que uma função de aquisição de chave é solicitada.

 

 

 




