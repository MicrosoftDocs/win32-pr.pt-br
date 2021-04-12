---
title: comutador/IID nomedearquivo
description: A opção/IID nomedearquivo especifica o nome do arquivo de identificador de interface para uma interface COM, substituindo o nome padrão obtido adicionando \_ i. c ao nome do arquivo IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL do comutador/IID nomedearquivo
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364946"
---
# <a name="iid-switch"></a>comutador/IID nomedearquivo

A opção **/IID nomedearquivo** especifica o nome do arquivo de identificador de interface para uma interface com, substituindo o nome padrão obtido adicionando \_ i. c ao nome do arquivo IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica um nome de arquivo de identificador de interface que substitui o nome de arquivo do identificador de interface padrão para uma interface COM. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/IID nomedearquivo** não afeta as interfaces RPC.

Se o *nome* do arquivo não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) . Um caminho explícito em *filename* substitui a especificação de opção **/out** .

## <a name="examples"></a>Exemplos

**MIDL/IID nomedearquivo "meu \_ IID. c" filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy nomedearquivo**](-proxy.md)
</dt> </dl>

 

 




