---
description: O método getvideoclipize recupera as dimensões de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Método getvídeos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105782245"
---
# <a name="getvideosize-method"></a>Método getvídeos

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetVideoSize` método recupera as dimensões de vídeo nativas.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valor Retornado

Retorna um objeto [DVDRect](dvdrect-object.md) contendo quatro propriedades de leitura/gravação: (superior esquerda) x; (superior esquerda) y, largura e altura. As propriedades **x** e **y** são definidas como zero e as outras duas propriedades refletem a largura e a altura do retângulo de vídeo como sendo criados no disco.

 

 



