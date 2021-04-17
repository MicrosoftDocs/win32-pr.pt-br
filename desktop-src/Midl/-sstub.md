---
title: comutador/sstub
description: A opção/sstub especifica o nome do arquivo stub do servidor para uma interface RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- MIDL do comutador/sstub
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105766250"
---
# <a name="sstub-switch"></a>comutador/sstub

A opção **/sstub** especifica o nome do arquivo stub do servidor para uma interface RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_nome do arquivo stub \_* 
</dt> <dd>

Especifica um nome de arquivo que substitui o nome de arquivo stub do servidor padrão. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome de arquivo especificado substitui o nome de arquivo padrão. Por padrão, o nome do arquivo é obtido adicionando \_ S. C ao nome do arquivo IDL. Essa opção não afeta as interfaces OLE.

Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo stub — o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.

Se *o \_ \_ nome do arquivo stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) . Um caminho explícito no *\_ \_ nome do arquivo de stub* substitui a especificação de opção **/out** .

A opção **/Server** None tem precedência sobre a opção **/sstub**

## <a name="examples"></a>Exemplos

**MIDL/sstub My \_ sstub. c filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




