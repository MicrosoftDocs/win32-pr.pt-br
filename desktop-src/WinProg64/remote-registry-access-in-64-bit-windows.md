---
title: Acesso remoto ao Registro em um servidor de 64 Windows
description: O redirecionador do Registro fornece acesso remoto ao Registro em 64 bits Windows por meio da função RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acesso remoto ao registro de programação Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561447"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Acesso remoto ao Registro em um servidor de 64 Windows

O redirecionador do Registro fornece acesso remoto ao Registro em Windows de 64 bits por meio da [**função RegConnectRegistry.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)

Se o cliente for um aplicativo de 32 bits, ele acessará a exibição padrão do Registro de 32 bits do servidor. Se o cliente for um aplicativo de 64 bits, ele acessará a exibição do Registro de 64 bits.

**Windows Server 2003:** Todos os clientes acessam a exibição do Registro de 64 bits, a menos que o aplicativo use o sinalizador KEY \_ WOW64 \_ 32KEY. Esse comportamento mudou com o Windows Server 2003 com o Service Pack 1 (SP1) e o Windows XP Professional x64 Edition, desde que o cliente e o servidor estão executando essas versões do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de Registro](registry-redirector.md)
</dt> <dt>

[Reflexão do Registro](registry-reflection.md)
</dt> </dl>

 

 