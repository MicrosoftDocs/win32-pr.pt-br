---
title: Opção/u
description: A opção/U remove qualquer definição anterior de um nome, passando o nome para o pré-processador de C como se fosse uma diretiva \ undefinetion.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U opção MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084185"
---
# <a name="u-switch"></a>Opção/u

A opção **/u** remove qualquer definição anterior de um nome, passando o nome para o pré-processador de C como se fosse uma diretiva **\# undefine** .

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*name* 
</dt> <dd>

Especifica um nome definido a ser passado para o pré-processador de C como se fosse uma diretiva **\# undefine** . O nome é predefinido pelo pré-processador C ou definido anteriormente pelo usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Várias diretivas **/u** podem ser usadas em uma linha de comando. O espaço em branco entre a opção **/u** e o nome indefinido é opcional.

Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela \_ opção cmd/cpp com as opções [**/i**](-i.md), [**/d**](-d.md)e **/u** e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF. A opção de compilador MIDL **/u** é ignorada quando o parâmetro de compilador MIDL switch **/ \_** **/cpp \_ opt** é especificado.

## <a name="examples"></a>Exemplos

**MIDL/UUNICODE filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ aceitar**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**///// \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




