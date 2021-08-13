---
title: Tratamento de exceções em WOW64
description: O WOW64 usa exceções nativas x64, ia64 ou ARM64 como um transporte para exceções x86. Portanto, em um aplicativo de 32 bits em execução em WOW64, exceções não ativas se comportam como exceções nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d461a809ac35a4742f9bdbbaeb461eb6d7365075d9c4b57334a94f434c1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561522"
---
# <a name="exception-handling-under-wow64"></a>Tratamento de exceções em WOW64

O WOW64 usa exceções nativas x64, ia64 ou ARM64 como um transporte para exceções x86. Portanto, em um aplicativo de 32 bits em execução em WOW64, exceções não ativas se comportam como exceções nativas de 64 bits.

Em um aplicativo em execução em uma versão de 32 bits do Windows, exceções não ativas são passadas para manipuladores de exceção de nível superior do aplicativo, quando disponíveis. No mesmo aplicativo de 32 bits em execução em WOW64, o sistema pode suprimir exceções não ativas.

**Windows Vista, Windows Server 2003 e Windows XP:** No mesmo aplicativo de 32 bits em execução em WOW64, o sistema chama os filtros de exceção, mas pode suprimir exceções não buscadas sem invocar os manipuladores associados. Esse comportamento mudou a partir do Windows Vista com Service Pack 1 (SP1).

Para obter mais informações sobre exceções não buscadas em procedimentos de janela, consulte a [função WindowProc.](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

 

 