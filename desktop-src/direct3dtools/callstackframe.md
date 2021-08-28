---
description: Representa informações sobre um quadro na callstack.
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
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631334"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Estrutura CallStackFrame

Representa informações sobre um quadro na callstack.

## <a name="syntax"></a>Sintaxe


```C++
} CallStackFrame;
```

## <a name="members"></a>Membros

**Functionname**  
Uma cadeia de caracteres COM que contém o nome da função associada.

**Sourcefile**  
Uma cadeia de caracteres COM que contém o caminho do arquivo de origem associado.

**moduleName**  
Uma cadeia de caracteres COM que contém o nome do módulo de código associado.

**Linenumber**  
O número de linha associado.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



