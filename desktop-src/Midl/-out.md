---
title: Opção /out
description: A opção/out especifica o diretório padrão em que o compilador MIDL grava os arquivos de saída.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- opção/out de MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105760693"
---
# <a name="out-switch"></a>Opção /out

A opção **/out** especifica o diretório padrão em que o compilador MIDL grava os arquivos de saída.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*especificação de caminho* 
</dt> <dd>

Especifica o caminho para o diretório no qual os arquivos stub, cabeçalho e comutador são gerados. Uma especificação de unidade, um caminho de diretório absoluto ou ambos podem ser especificados. Os caminhos podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O diretório de saída pode ser especificado com uma letra de unidade, um nome de caminho absoluto ou ambos. A opção **/out** pode ser usada com qualquer uma das opções que habilitam a especificação de arquivo de saída individual.

Quando a opção **/out** não é especificada, os arquivos são gravados no diretório atual.

O diretório padrão especificado pela opção **/out** pode ser substituído por um nome de caminho explícito especificado como parte da opção [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy nomedearquivo**](-proxy.md)ou [**/sstub**](-sstub.md) .

## <a name="examples"></a>Exemplos

**MIDL/out c: \\ mydir \\ mysubdir \\ subdir2 mais profundo nome do arquivo. idl**

**MIDL/out c: filename. idl**

**MIDL/out \\ mydir \\ mysubdir \\ outro nome de arquivo. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy nomedearquivo**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




