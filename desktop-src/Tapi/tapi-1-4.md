---
description: A TAPI 1,4 adicionou várias APIs, mensagens, constantes e elementos de estrutura à especificação de 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921690"
---
# <a name="tapi-14"></a>TAPI 1,4

A TAPI 1,4 adicionou várias APIs, mensagens, constantes e elementos de estrutura à especificação de 1,3. A TAPI 1,4 dá suporte apenas a TSPs de 16 bits. No entanto, ele permite que os aplicativos de 32 bits sejam desenvolvidos sem a necessidade de se preocupar com as limitações do Windows de 16 bits.

Os arquivos de cabeçalho TAPI e TSPI são usados para desenvolver ambos os aplicativos para TAPI 1,4 e TAPI 2. x. Embora não haja muitas alterações nas estruturas entre essas duas especificações, houve alterações na API (especificamente, suporte a Unicode) que tornam muito importante observar que os cabeçalhos são compilados de forma diferente, dependendo da \_ constante da versão atual da TAPI \_ . Por exemplo:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> \_ \_ A versão atual da TAPI deve ser definida para todos os aplicativos TAPI. Embora não seja estritamente necessário para o desenvolvimento da TAPI 2. x, podem ocorrer alterações futuras para exigir isso.

 

 

 



