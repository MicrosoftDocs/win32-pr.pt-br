---
title: Opção /tlb
description: A opção /tlb especifica um nome de arquivo para a biblioteca de tipos gerada pelo compilador MIDL.
ms.assetid: 7d5d9f92-ed1a-46bc-beb1-4be70d0a4813
keywords:
- /tlb switch MIDL
topic_type:
- apiref
api_name:
- /tlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081723648788ec51fa65a4770deb336f665804a9527dc223000826870dbe1ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643746"
---
# <a name="tlb-switch"></a>Opção /tlb

A **opção /tlb** especifica um nome de arquivo para a biblioteca de tipos gerada pelo compilador MIDL.

``` syntax
midl /tlb filename
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*Filename* 
</dt> <dd>

Especifica o nome do arquivo TLB (biblioteca de tipos de saída). Por padrão, se a **opção /tlb** não for usada, o arquivo TLB terá o mesmo nome que o arquivo IDL, com a extensão . Tlb.

</dd> </dl>

## <a name="examples"></a>Exemplos

**midl /tlb newname.tlb**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/notlb**](-notlb.md)
</dt> </dl>

 

 




