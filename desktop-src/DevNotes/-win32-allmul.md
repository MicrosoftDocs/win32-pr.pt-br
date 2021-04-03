---
title: Rotina de _allmul
description: Multiplica dois inteiros LONGLONG ou ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104007025"
---
# <a name="_allmul-routine"></a>\_Rotina allmul

Multiplica dois inteiros **LONGLONG** ou **ULONGLONG** .
Por exemplo, para multiplicar dois valores Int64, o compilador pode gerar uma chamada para a rotina **\_ allmul** .

## <a name="remarks"></a>Comentários

A rotina **\_ allmul** é uma rotina auxiliar para o compilador C.
Se o compilador usa **\_ allmul** é completamente dependente do conjunto de otimização.

Essa rotina é usada somente em plataformas x86.
