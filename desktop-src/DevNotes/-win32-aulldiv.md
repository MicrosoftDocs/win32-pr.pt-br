---
title: Rotina de _aulldiv
description: Divide dois inteiros ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538896"
---
# <a name="_aulldiv-routine"></a>\_Rotina aulldiv

Divide dois inteiros **ULONGLONG** .
Por exemplo, para dividir dois valores UInt64, o compilador pode gerar uma chamada para a rotina **\_ aulldiv** .

## <a name="remarks"></a>Comentários

A rotina **\_ aulldiv** é uma rotina auxiliar para o compilador C.
Se o compilador usa **\_ aulldiv** é completamente dependente do conjunto de otimização.

Essa função é usada somente em plataformas x86.
