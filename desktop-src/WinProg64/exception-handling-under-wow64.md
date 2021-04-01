---
title: Tratamento de exceção sob WOW64
description: O WOW64 usa exceções nativas x64, IA64 ou ARM64 como um transporte para exceções x86. Portanto, em um aplicativo de 32 bits em execução no WOW64, exceções não capturadas se comportam como exceções nativas de 64 bits.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008028"
---
# <a name="exception-handling-under-wow64"></a>Tratamento de exceção sob WOW64

O WOW64 usa exceções nativas x64, IA64 ou ARM64 como um transporte para exceções x86. Portanto, em um aplicativo de 32 bits em execução no WOW64, exceções não capturadas se comportam como exceções nativas de 64 bits.

Em um aplicativo executado em uma versão de 32 bits do Windows, exceções não capturadas são passadas para manipuladores de exceção de nível superior do aplicativo, quando disponíveis. No mesmo aplicativo de 32 bits em execução no WOW64, o sistema pode suprimir exceções não capturadas.

**Windows Vista, Windows Server 2003 e Windows XP:** No mesmo aplicativo de 32 bits em execução no WOW64, o sistema chama os filtros de exceção, mas pode suprimir exceções não capturadas sem invocar os manipuladores associados. Esse comportamento mudou a partir do Windows Vista com Service Pack 1 (SP1).

Para obter mais informações sobre exceções não capturadas em procedimentos de janela, consulte a função [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

 

 