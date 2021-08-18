---
title: Opção /notlb
description: A opção /notlb impede que o compilador MIDL gere um arquivo TLB (biblioteca de tipos).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb switch MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067516"
---
# <a name="notlb-switch"></a>Opção /notlb

A **opção /notlb** impede que o compilador MIDL gere um arquivo TLB (biblioteca de tipos).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Por padrão, o compilador MIDL gerará um arquivo TLB sempre que encontrar uma [**instrução LIBRARY.**](library.md) Essa opção substitui o comportamento padrão.

Quando a **opção /notlb** é especificada, todos os outros stubs, headers etc. são gerados como de costume.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




