---
title: comutador/env
description: A opção/env seleciona o ambiente no qual o aplicativo é executado.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL do comutador/env
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365882"
---
# <a name="env-switch"></a>comutador/env

A opção **/env** seleciona o ambiente no qual o aplicativo é executado.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 32 bits.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>IA64 * * * *


</dt> <dd>

Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de arquitetura Intel de 64 bits (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>AMD64 * * * * *


</dt> <dd>

Direciona o compilador MIDL para gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente avançado de micro dispositivos 64 bits (AMD64).

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * *


</dt> <dd>

Mesmo comportamento que *IA64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/env** afeta principalmente o nível de embalagem usado para estruturas nesse ambiente. Certifique-se de especificar a mesma configuração de nível de embalagem para o compilador de MIDL e o compilador do C.

A opção **/env** determina o nível de embalagem e outras configurações da seguinte maneira:

-   Quando você especifica o **Win32**, os stubs gerados usam o nível de empacotamento do C-Compiler 8 para todos os tipos envolvidos em operações remotas. Os tipos de dados [**int**](int.md) são 32 bits. Os ponteiros são 32 bits.
-   Quando você especifica **IA64** ou **AMD64**, o compilador MIDL é executado em um modo de compilador cruzado para a plataforma indicada (Intel ou AMD) 64 bits. Os stubs gerados usam o nível de empacotamento do C-Compiler 8 para todos os tipos envolvidos em operações remotas. Os tipos de dados [**Long**](long.md) e [**int**](int.md) são 32 bits. Os ponteiros são 64 bits.

Os comutadores [**/align**](-align.md), [**/Pack**](-pack.md)e [**/ZP**](-zp.md) têm precedência sobre as configurações de **/env** .

Para obter mais informações sobre o suporte de 64 bits para MIDL e RPC [, consulte Projetando interfaces compatíveis com 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Exemplos

**MIDL/Env Win32 nomedoarquivo. idl**

**MIDL/Env IA64 filename. idl**

**MIDL/Env AMD64 nomedoarquivo. idl**

**MIDL/Env Win64 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 