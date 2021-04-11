---
title: comutador/Win64
description: A opção/Win64 instrui o compilador MIDL a gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 64 bits. Observe que essa opção está obsoleta.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- MIDL do comutador/Win64
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293112"
---
# <a name="win64-switch"></a>comutador/Win64

A opção **/Win64** instrui o compilador MIDL a gerar arquivos stub, ou um arquivo de biblioteca de tipos, para um ambiente de 64 bits.

> [!Note]  
> Essa opção é obsoleta. Em vez disso, use a opção [**/IA64**](-ia64.md) ou [**/AMD64**](-amd64.md) . A opção **/Win64** é equivalente à opção **/IA64** .

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

A opção **/Win64** é equivalente a definir a opção [**/env**](-env.md) como Win64.

> [!Note]  
> Não é possível usar MIDL.exe para produzir um TLB de 64 bits no Windows 2000.

 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




