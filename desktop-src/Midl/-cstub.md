---
title: comutador/cstub
description: A opção/cstub especifica o nome do arquivo stub do cliente para uma interface RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- MIDL do comutador/cstub
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293332"
---
# <a name="cstub-switch"></a>comutador/cstub

A opção **/cstub** especifica o nome do arquivo stub do cliente para uma interface RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_nome do arquivo stub \_* 
</dt> <dd>

Especifica um nome de arquivo que substitui o nome de arquivo stub do cliente padrão. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome de arquivo especificado substitui o nome de arquivo padrão. Por padrão, o nome do arquivo é obtido adicionando a extensão \_ c. c ao nome do arquivo IDL. Essa opção não afeta as interfaces OLE.

Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo stub — o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.

Se *o \_ \_ nome do arquivo stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) . Um caminho explícito no *\_ \_ nome do arquivo de stub* substitui a especificação de opção **/out** .

A opção **/Client** None tem precedência sobre a opção **/cstub**

## <a name="examples"></a>Exemplos

**MIDL/cstub My \_ cstub. c filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




