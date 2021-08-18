---
title: Opção /mktyplib203
description: A opção /mktyplib203 força o compilador MIDL a analisar o arquivo de entrada.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 switch MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014144"
---
# <a name="mktyplib203-switch"></a>Opção /mktyplib203

A **opção /mktyplib203** força o compilador MIDL a analisar o arquivo de entrada.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Para usar a opção **/mktyplib203,** o arquivo de entrada deve seguir exatamente a sintaxe ODL, o que significa que você não pode colocar instruções fora do bloco de biblioteca. Exemplos

**midl /mktyplib203 myoldodl.odl**

**midl /mktyplib203 oldhabit.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




