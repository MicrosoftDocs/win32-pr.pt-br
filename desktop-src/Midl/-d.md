---
title: Opção/d
description: A opção/D define um nome e um valor opcional a ser passado para o pré-processador de C como se fosse uma diretiva \ define. Várias diretivas/D podem ser usadas em uma linha de comando.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D opção MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084208"
---
# <a name="d-switch"></a>Opção/d

A opção **/d** define um nome e um valor opcional a ser passado para o pré-processador de C como se fosse por uma diretiva de **\# definição** . Várias diretivas **/d** podem ser usadas em uma linha de comando.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*name* 
</dt> <dd>

Especifica um nome definido que é passado para o pré-processador C quando a opção [**/cpp \_ cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não está presente.

</dd> <dt>

*defini* 
</dt> <dd>

Especifica um valor associado ao nome definido.

</dd> </dl>

## <a name="remarks"></a>Comentários

O espaço em branco entre a opção **/d** e o nome definido é opcional.

Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela opção **\_ cmd/cpp** com as opções [**/i**](-i.md), **/d** e [**/U**](-u.md) e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF.

A opção de compilador MIDL **/d** é ignorada quando o parâmetro de compilador MIDL switch [/ \_](-no-cpp-nocpp.md) [**/cpp \_ opt**](-cpp-opt.md) é especificado.

## <a name="examples"></a>Exemplos

**MIDL-DUNICODE filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ aceitar**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**///// \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 




