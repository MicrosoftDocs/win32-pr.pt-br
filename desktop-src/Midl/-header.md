---
title: Opção /header
description: A opção /header especifica o nome do arquivo de header.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header switch MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde032d611cb09f3da2d048bfab85bd3b0a1c8aadebf251fe8c01ecd8630a36e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808966"
---
# <a name="header-switch"></a>Opção /header

A **opção /header** especifica o nome do arquivo de header.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*Filename* 
</dt> <dd>

Especifica um nome de arquivo de header que substitui o nome do arquivo de header padrão. Os nomes de arquivo podem ser explicitamente entre aspas duplas (") para impedir que o shell interprete caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome do arquivo especificado substitui o nome de arquivo padrão. O nome de arquivo padrão é obtido substituindo a extensão de nome de arquivo IDL (geralmente .idl) pela extensão de nome de arquivo .h. Para interfaces OLE, a **opção /header** substitui o nome padrão do arquivo de header da interface.

Quando você está importando arquivos, o nome do arquivo especificado se aplica a apenas um arquivo de header – o arquivo de header que corresponde ao arquivo IDL especificado na linha de comando.

Se *filename* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela [**opção /out.**](-out.md) Um caminho explícito no *nome do arquivo* substitui a **especificação da opção /out.**

## <a name="examples"></a>Exemplos

**midl /header "bar.h" filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




