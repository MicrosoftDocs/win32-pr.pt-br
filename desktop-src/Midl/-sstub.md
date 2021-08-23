---
title: /sstub switch
description: A opção /sstub especifica o nome do arquivo stub do servidor para uma interface RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub switch MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd83776939e9746103b2f12598a53832d767cebb93767142649a09b804339a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014064"
---
# <a name="sstub-switch"></a>/sstub switch

A **opção /sstub** especifica o nome do arquivo stub do servidor para uma interface RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*nome do arquivo stub \_ \_* 
</dt> <dd>

Especifica um nome de arquivo que substitui o nome do arquivo stub do servidor padrão. Os nomes de arquivo podem ser explicitamente entre aspas duplas (") para impedir que o shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome do arquivo especificado substitui o nome de arquivo padrão. Por padrão, o nome do arquivo é obtido adicionando \_ S.C ao nome do arquivo IDL. Essa opção não afeta as interfaces OLE.

Quando você está importando arquivos, o nome do arquivo especificado se aplica a apenas um arquivo stub – o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.

Se *o nome do \_ arquivo \_ stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela [**opção /out.**](-out.md) Um caminho explícito no nome *do arquivo stub \_ \_* substitui a **especificação da opção /out.**

A **opção /server** none tem precedência sobre a **opção /sstub.**

## <a name="examples"></a>Exemplos

**midl /sstub my \_ sstub.c filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




