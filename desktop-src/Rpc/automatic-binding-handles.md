---
title: Identificadores de associação automática
description: Os identificadores de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294386"
---
# <a name="automatic-binding-handles"></a>Identificadores de associação automática

Os identificadores de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor. Quando você usa um identificador de ligação automática, não precisa escrever nenhum código de aplicativo cliente para lidar com associações e identificadores — basta especificar o uso do identificador de ligação automática no arquivo de configuração de aplicativo (ACF). Em seguida, o stub define o identificador e gerencia a associação.

Por exemplo, uma operação de carimbo de data/hora pode ser implementada usando um identificador automático. Não faz diferença ao aplicativo cliente que o servidor fornece com o carimbo de data/hora, pois ele pode aceitar o tempo de qualquer servidor disponível.

> [!Note]  
> Os identificadores automáticos não têm suporte para a plataforma Macintosh.

 

Você especifica o uso de identificadores automáticos, incluindo o atributo de \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] no ACF. O exemplo de carimbo de data/hora usa o seguinte ACF:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Quando o ACF não inclui nenhum outro atributo de identificador e quando os procedimentos remotos não usam identificadores explícitos, o compilador MIDL usa identificadores automáticos por padrão. Ele também usa identificadores automáticos como padrão quando o ACF não está presente.

Os procedimentos remotos são especificados no arquivo IDL. O identificador automático não deve aparecer como um argumento para o procedimento remoto. Por exemplo:

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

O benefício do identificador automático é que o desenvolvedor não precisa escrever nenhum código para gerenciar o identificador; os stubs gerenciam a associação automaticamente. Isso é significativamente diferente do [exemplo Hello, World](tutorial.md), em que o cliente gerencia o identificador primitivo implícito definido no ACF e deve chamar várias funções de tempo de execução para estabelecer o identificador de associação.

 

 