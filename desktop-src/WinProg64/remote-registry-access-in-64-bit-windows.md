---
title: Acesso remoto ao registro no Windows de 64 bits
description: O redirecionador de registro fornece acesso remoto ao registro em janelas de 64 bits por meio da função RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acesso remoto ao registro, programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790451"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Acesso remoto ao registro no Windows de 64 bits

O redirecionador de registro fornece acesso remoto ao registro em janelas de 64 bits por meio da função [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Se o cliente for um aplicativo de 32 bits, ele acessará a exibição do registro padrão de 32 bits do servidor. Se o cliente for um aplicativo de 64 bits, ele acessará a exibição do registro de 64 bits.

**Windows Server 2003:** Todos os clientes acessam a exibição de registro de 64 bits, a menos que o aplicativo use o \_ sinalizador 32KEY de WOW64 de chave \_ . Esse comportamento mudou com o Windows Server 2003 com Service Pack 1 (SP1) e o Windows XP Professional x64 Edition, desde que o cliente e o servidor estejam executando essas versões do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de registro](registry-redirector.md)
</dt> <dt>

[Reflexão do registro](registry-reflection.md)
</dt> </dl>

 

 