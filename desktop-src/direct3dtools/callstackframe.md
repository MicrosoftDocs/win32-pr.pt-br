---
description: Representa informações sobre um quadro na pilha de chamadas.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura CallStackFrame
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813456"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Estrutura CallStackFrame

Representa informações sobre um quadro na pilha de chamadas.

## <a name="syntax"></a>Sintaxe


```C++
} CallStackFrame;
```

## <a name="members"></a>Membros

**functionName**  
Uma cadeia de caracteres COM que contém o nome da função associada.

**sourceFile**  
Uma cadeia de caracteres COM que contém o caminho de arquivo de origem associado.

**moduleName**  
Uma cadeia de caracteres COM que contém o nome do módulo de código associado.

**lineNumber**  
O número da linha associada.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



