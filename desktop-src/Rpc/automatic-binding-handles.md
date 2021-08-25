---
title: Alças de associação automática
description: Os alças de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b619b17e44e79e623bcffa84f4938d1278a7d146d6de90547cd833e1bf091167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023436"
---
# <a name="automatic-binding-handles"></a>Alças de associação automática

Os alças de associação automática são úteis quando o aplicativo não requer um servidor específico e quando não precisa manter nenhuma informação de estado entre o cliente e o servidor. Ao usar um alça de associação automática, você não precisa escrever nenhum código de aplicativo cliente para lidar com a associação e os alças– basta especificar o uso do alça de associação automática no arquivo de configuração de aplicativo (ACF). Em seguida, o stub define o handle e gerencia a associação.

Por exemplo, uma operação de carimbo de data/hora pode ser implementada usando uma alça automática. Não faz diferença para o aplicativo cliente que o servidor fornece o carimbo de data/hora, pois ele pode aceitar a hora de qualquer servidor disponível.

> [!Note]  
> Não há suporte para alças automáticas para a plataforma Macintosh.

 

Especifique o uso de alças automáticas incluindo o atributo \[ [**de \_ alça**](/windows/desktop/Midl/auto-handle) \] automática no ACF. O exemplo de carimbo de data/hora usa o seguinte ACF:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Quando o ACF não inclui nenhum outro atributo de handle e quando os procedimentos remotos não usam alças explícitas, o compilador MIDL usa alças automáticas por padrão. Ele também usa alças automáticas como o padrão quando o ACF não está presente.

Os procedimentos remotos são especificados no arquivo IDL. O handle automático não deve aparecer como um argumento para o procedimento remoto. Por exemplo:

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

O benefício do controle automático é que o desenvolvedor não precisa escrever nenhum código para gerenciar o handle; os stubs gerenciam a associação automaticamente. Isso é significativamente diferente do exemplo [Hello, World,](tutorial.md)em que o cliente gerencia o handle primitivo implícito definido no ACF e deve chamar várias funções de tempo de run time para estabelecer o alça de associação.

 

 