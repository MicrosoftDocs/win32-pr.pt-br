---
title: comutador/Client
description: A opção/Client instrui o compilador MIDL a gerar arquivos de origem C do lado do cliente para uma interface RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL do comutador/Client
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293333"
---
# <a name="client-switch"></a>comutador/Client

A opção **/Client** instrui o compilador MIDL a gerar arquivos de origem C do lado do cliente para uma interface RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * * *


</dt> <dd>

Gera os arquivos do lado do cliente.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nenhum * * * *


</dt> <dd>

Não gera nenhum arquivo do lado do cliente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Quando a opção **/Client** não é especificada, o compilador MIDL gera o arquivo stub do cliente. Essa opção não afeta as interfaces OLE.

A opção **/Client** tem precedência sobre a opção [**/cstub**](-cstub.md)

## <a name="examples"></a>Exemplos

**MIDL/Client None filename. idl**

**nome de arquivo stub/Client de MIDL. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




