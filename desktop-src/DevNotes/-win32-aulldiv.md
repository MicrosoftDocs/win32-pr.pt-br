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
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104453836"
---
# <a name="_aulldiv-routine"></a>\_Rotina aulldiv

Divide dois inteiros **ULONGLONG** .
Por exemplo, para dividir dois valores UInt64, o compilador pode gerar uma chamada para a rotina **\_ aulldiv** .

## <a name="remarks"></a>Comentários

A rotina **\_ aulldiv** é uma rotina auxiliar para o compilador C.
Se o compilador usa **\_ aulldiv** é completamente dependente do conjunto de otimização.

Essa função é usada somente em plataformas x86.
