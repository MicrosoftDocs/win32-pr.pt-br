---
title: opção/Server
description: A opção/Server direciona o compilador MIDL para gerar arquivos de origem C do lado do servidor para uma interface RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /Server switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006562"
---
# <a name="server-switch"></a>opção/Server

A opção **/Server** direciona o compilador MIDL para gerar arquivos de origem C do lado do servidor para uma interface RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * * *


</dt> <dd>

Gera os arquivos do lado do servidor.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nenhum * * * *


</dt> <dd>

Não gera arquivos do lado do servidor.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Quando a opção **/Server** não é especificada, o compilador MIDL gera o arquivo stub do servidor. Essa opção não afeta as interfaces OLE.

A opção **None** não faz com que nenhum arquivo seja gerado.

A opção **/Server** tem precedência sobre a opção **/sstub**

## <a name="examples"></a>Exemplos

**MIDL/Server None**

**stub do MIDL/Server**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




