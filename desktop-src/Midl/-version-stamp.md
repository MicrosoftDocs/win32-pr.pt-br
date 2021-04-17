---
title: opção/version_stamp
description: A \_ opção de carimbo/Version suprime a geração de macros que especificam o número de versão mínimo necessário do arquivo de cabeçalho RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp MIDL do comutador
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105812920"
---
# <a name="version_stamp-switch"></a>\_opção de carimbo/Version

A opção de **\_ carimbo/Version** suprime a geração de macros que especificam o número de versão mínimo necessário do arquivo de cabeçalho RPC, Rpcndr. h.

Os novos recursos de MIDL podem exigir definições adicionais para compilar o stub corretamente, portanto, o stub tem macros que verificam a compatibilidade entre arquivos binários de MIDL e o ambiente de compilação. Talvez seja necessário usar essa opção se você mover MIDL para um ambiente de compilação diferente daquele em que você instalou os arquivos binários de MIDL pela primeira vez.

Observe que não há suporte para a combinação de ambientes de compilação.

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

 

 




