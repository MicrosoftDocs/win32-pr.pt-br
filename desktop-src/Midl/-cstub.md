---
title: /cstub switch
description: A opção /cstub especifica o nome do arquivo stub do cliente para uma interface RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub switch MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b4f635b6d09c85b345eea6dcb7320294e226ad6f2540f01af1e9b3e8098671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105653"
---
# <a name="cstub-switch"></a>/cstub switch

A **opção /cstub** especifica o nome do arquivo stub do cliente para uma interface RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*nome do arquivo stub \_ \_* 
</dt> <dd>

Especifica um nome de arquivo que substitui o nome de arquivo de stub do cliente padrão. Os nomes de arquivo podem ser explicitamente entre aspas duplas (") para impedir que o shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome do arquivo especificado substitui o nome de arquivo padrão. Por padrão, o nome do arquivo é obtido adicionando a extensão \_ c.c ao nome do arquivo IDL. Essa opção não afeta as interfaces OLE.

Quando você está importando arquivos, o nome do arquivo especificado se aplica a apenas um arquivo stub – o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.

Se *o nome do \_ arquivo \_ stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela [**opção /out.**](-out.md) Um caminho explícito no nome *do arquivo stub \_ \_* substitui a **especificação da opção /out.**

A **opção /client** none tem precedência sobre a **opção /cstub.**

## <a name="examples"></a>Exemplos

**midl /cstub my \_ cstub.c filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




