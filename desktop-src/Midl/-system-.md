---
title: /comutador do sistema
description: O comutador/sistema direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado. O padrão é o sistema operacional atual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /comutador do sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01b6455807aedb99d7bd525c69fffc524dbe25d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882789"
---
# <a name="ltsystemgt-switch"></a>/&lt;&gt;comutador do sistema

A opção **/ &lt; System &gt;** direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado. O padrão é o sistema operacional atual.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>IA64 * * * *


</dt> <dd>

um ambiente de Windows de 64 bits baseado em Intel, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista ou Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * * *


</dt> <dd>

um ambiente de Windows de 64 bits com base no American Micro dispositivos, como Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista ou Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

O comutador do **/ &lt; sistema &gt;** é funcionalmente o mesmo que a opção MIDL [**/env**](-env.md) e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib. Se você estiver gerando um novo makefile, use a opção **/env** .

## <a name="examples"></a>Exemplos

**MIDL/Win32 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




