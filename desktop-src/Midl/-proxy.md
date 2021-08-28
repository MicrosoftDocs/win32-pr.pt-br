---
title: comutador/proxy nomedearquivo
description: A opção/proxy nomedearquivo especifica o nome do arquivo de proxy de interface para uma interface COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- MIDL do comutador/proxy nomedearquivo
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc3483706369837d96d14cf30b2f0c6ee307e376f8c422e11d56e06451a22e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811206"
---
# <a name="proxy-switch"></a>comutador/proxy nomedearquivo

A opção **/proxy nomedearquivo** especifica o nome do arquivo de proxy de interface para uma interface com.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*\_nome do arquivo de proxy \_* 
</dt> <dd>

Especifica um nome de arquivo que substitui o nome de arquivo de proxy de interface padrão. Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nome de arquivo especificado substitui o nome de arquivo padrão obtido adicionando \_ P. C ao nome do arquivo IDL. O comutador/ [**proxy**](proxy.md) não afeta as interfaces RPC.

Se *o \_ \_ nome do arquivo de proxy* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) . Um caminho explícito no *\_ \_ nome do arquivo de proxy* substitui a especificação de opção **/out** .

Para obter uma descrição mais detalhada do arquivo de proxy de interface e outros arquivos gerados pelo compilador MIDL, consulte [sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md).

## <a name="examples"></a>Exemplos

**MIDL/proxy nomedearquivo My \_ proxy. c filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/IID nomedearquivo**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




