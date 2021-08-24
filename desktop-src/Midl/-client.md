---
title: /client switch
description: A opção /client direciona o compilador MIDL para gerar arquivos de origem C do lado do cliente para uma interface RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client switch MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8361a41aa0e7c87c42eb41508fee0973d6fd4dd821e2008aa2148c8460fc63ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764356"
---
# <a name="client-switch"></a>/client switch

A **opção /client** direciona o compilador MIDL para gerar arquivos de origem C do lado do cliente para uma interface RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub****


</dt> <dd>

Gera os arquivos do lado do cliente.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none****


</dt> <dd>

Não gera nenhum arquivo do lado do cliente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Quando a **opção /client** não for especificada, o compilador MIDL gerará o arquivo stub do cliente. Essa opção não afeta as interfaces OLE.

A **opção /client** tem precedência sobre a [**opção /cstub.**](-cstub.md)

## <a name="examples"></a>Exemplos

**midl /client none filename.idl**

**midl /client stub filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/server**](-server.md)
</dt> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




