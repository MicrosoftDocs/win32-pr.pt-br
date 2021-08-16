---
title: /opção do sistema
description: A opção /system direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado. O padrão é o sistema operacional atual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /system switch MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31def6297a1a91f6ed28943290a66b544dc368d5a00a91932035a338af50bac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643774"
---
# <a name="system-switch"></a>/<system> Interruptor

A **/<system>** opção direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado. O padrão é o sistema operacional atual.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32****


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64****


</dt> <dd>

Um ambiente de Windows baseado em Intel de 64 bits, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista ou Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64****


</dt> <dd>

Um ambiente de Windows de 64 bits baseado em Micro Devices americano, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista ou Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A opção é funcionalmente a mesma que a opção /env MIDL e é reconhecida pelo compilador MIDL exclusivamente para compatibilidade com compatibilidade com corretamente com **/<system>** MkTypLib. [](-env.md) Se você estiver gerando um novo makefile, use a **opção /env.**

## <a name="examples"></a>Exemplos

**midl /win32 filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




