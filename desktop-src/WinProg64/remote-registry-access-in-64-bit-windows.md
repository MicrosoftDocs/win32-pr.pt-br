---
title: Acesso remoto ao registro no Windows de 64 bits
description: o redirecionador de registro fornece acesso remoto ao registro no Windows de 64 bits por meio da função RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acesso ao registro remoto 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561447"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Acesso remoto ao registro no Windows de 64 bits

o redirecionador de registro fornece acesso remoto ao registro no Windows de 64 bits por meio da função [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Se o cliente for um aplicativo de 32 bits, ele acessará a exibição do registro padrão de 32 bits do servidor. Se o cliente for um aplicativo de 64 bits, ele acessará a exibição do registro de 64 bits.

**Windows Server 2003:** Todos os clientes acessam a exibição de registro de 64 bits, a menos que o aplicativo use o \_ sinalizador 32KEY de WOW64 de chave \_ . esse comportamento mudou com Windows Server 2003 com Service Pack 1 (SP1) e Windows XP Professional x64 Edition, desde que o cliente e o servidor estejam executando essas versões do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de registro](registry-redirector.md)
</dt> <dt>

[Reflexão do registro](registry-reflection.md)
</dt> </dl>

 

 