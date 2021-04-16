---
title: comutador/notlb
description: A opção/notlb impede que o compilador MIDL gere um arquivo de biblioteca de tipos (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL do comutador/notlb
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453777"
---
# <a name="notlb-switch"></a>comutador/notlb

A opção **/notlb** impede que o compilador MIDL gere um arquivo de biblioteca de tipos (tlb).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Por padrão, o compilador MIDL irá gerar um arquivo TLB sempre que encontrar uma instrução de [**biblioteca**](library.md) . Essa opção substitui o comportamento padrão.

Quando a opção **/notlb** é especificada, todos os outros stubs, cabeçalhos, etc. são gerados como de costume.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




