---
title: Opção /U
description: A opção /U remove qualquer definição anterior de um nome passando o nome para o pré-processador C como se fosse por uma diretiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U switch MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895766"
---
# <a name="u-switch"></a>Opção /U

A **opção /U** remove qualquer definição anterior de um nome passando o nome para o pré-processador C como se fosse por uma diretiva **\# indefinida.**

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*name* 
</dt> <dd>

Especifica um nome definido a ser passado para o pré-processador C como se fosse por uma diretiva **\# ineficaz.** O nome é predefinido pelo pré-processador C ou definido anteriormente pelo usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Várias **diretivas /U** podem ser usadas em uma linha de comando. O espaço em branco **entre a opção /U** e o nome indefinido é opcional.

Quando a opção [**/cpp \_ cmd**](-cpp-cmd.md) está presente e a opção [**/cpp \_ opt**](-cpp-opt.md) não está, o compilador MIDL concatena a cadeia de caracteres especificada pela opção /cpp cmd com as opções \_ [**/I,**](-i.md) [**/D**](-d.md)e **/U** e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF. A opção **/U** do compilador MIDL é ignorada quando a opção do compilador MIDL **/no \_ cpp** ou **/cpp \_ opt** é especificada.

## <a name="examples"></a>Exemplos

**midl /UUNICODE filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/d**](-d.md)
</dt> <dt>

[**/i**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




