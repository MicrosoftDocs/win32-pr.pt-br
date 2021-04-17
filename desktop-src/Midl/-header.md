---
title: comutador/header
description: A opção/header especifica o nome do arquivo de cabeçalho.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- MIDL do comutador/header
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364948"
---
# <a name="header-switch"></a>comutador/header

A opção **/header** especifica o nome do arquivo de cabeçalho.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica um nome de arquivo de cabeçalho que substitui o nome do arquivo de cabeçalho padrão. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome de arquivo especificado substitui o nome de arquivo padrão. O nome de arquivo padrão é obtido substituindo a extensão de nome de arquivo IDL (normalmente. idl) pela extensão de nome de arquivo. h. Para interfaces OLE, a opção **/header** substitui o nome padrão do arquivo de cabeçalho da interface.

Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo de cabeçalho — o arquivo de cabeçalho que corresponde ao arquivo IDL especificado na linha de comando.

Se o *nome* do arquivo não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) . Um caminho explícito em *filename* substitui a especificação de opção **/out** .

## <a name="examples"></a>Exemplos

**MIDL/Header "bar. h" filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy nomedearquivo**](-proxy.md)
</dt> </dl>

 

 




