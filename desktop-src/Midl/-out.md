---
title: Opção /out
description: A opção /out especifica o diretório padrão em que o compilador MIDL grava arquivos de saída.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out switch MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b29c97438c0db1a60d94a8ae88ed99f73c33ea16a820d1aec5ca7a6be737e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014094"
---
# <a name="out-switch"></a>Opção /out

A **opção /out** especifica o diretório padrão em que o compilador MIDL grava arquivos de saída.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*especificação de caminho* 
</dt> <dd>

Especifica o caminho para o diretório no qual os arquivos stub, header e switch são gerados. Uma especificação de unidade, um caminho de diretório absoluto ou ambos podem ser especificados. Os caminhos podem ser explicitamente entre aspas duplas (") para impedir que o shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O diretório de saída pode ser especificado com uma letra da unidade, um nome de caminho absoluto ou ambos. A **opção /out** pode ser usada com qualquer uma das opções que habilitam a especificação de arquivo de saída individual.

Quando a **opção /out** não é especificada, os arquivos são gravados no diretório atual.

O diretório padrão especificado pela opção **/out** pode ser substituído por um nome de caminho explícito especificado como parte da opção [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)ou [**/sstub.**](-sstub.md)

## <a name="examples"></a>Exemplos

**midl /out c: \\ mydir \\ mysubdir \\ subdir2 deeper filename.idl**

**midl /out c: filename.idl**

**midl /out \\ mydir \\ mysubdir \\ another filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




