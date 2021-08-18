---
description: A propriedade FramesPerSecond recupera a taxa de quadros de vídeo para o título do DVD atual.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propriedade FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a883f031680a57711fa092f29bc9ecbd76cb1a017c03f80337959050e62cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015664"
---
# <a name="framespersecond-property"></a>Propriedade FramesPerSecond

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `FramesPerSecond` propriedade recupera a taxa de quadros de vídeo para o título do DVD atual.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa a taxa de quadros de vídeo; 25 ou 30 quadros por segundo.

## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura sem valor padrão. Os sinais de vídeo NTSC são exibidos a 30 quadros por segundo. PAL é exibido em 25 quadros por segundo. Um disco é codificado para reproduzir em NTSC ou PAL, mas não pode ser reproduzir em ambos.

 

 



