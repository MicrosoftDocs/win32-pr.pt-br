---
title: opção/h
description: A opção/h é funcionalmente equivalente à opção/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h alternar MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71bf02668a583b330684338cbc3f639fbbda5a340c7226e10956233aa8dc9ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105606"
---
# <a name="h-switch"></a>opção/h

A opção **/h** é funcionalmente equivalente à opção [**/header**](-header.md) .

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica um nome de arquivo de cabeçalho que substitui o nome do arquivo de cabeçalho padrão. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/h** especifica *filename* como o nome de um arquivo de cabeçalho que contém todas as definições contidas no arquivo IDL sem a sintaxe IDL. Esse arquivo pode ser usado como um arquivo de cabeçalho C ou C++.

## <a name="examples"></a>Exemplos

**MIDL/h tlibhead. h filename. idl**

**MIDL/h "MIDL. h" filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




