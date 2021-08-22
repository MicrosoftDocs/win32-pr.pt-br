---
description: O método GetVideoSize recupera as dimensões de vídeo nativas.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Método GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21746242211357e9e58e825d8e217799953dd569e91765acabe11fc2252d17c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536586"
---
# <a name="getvideosize-method"></a>Método GetVideoSize

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetVideoSize` método recupera as dimensões de vídeo nativas.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valor Retornado

Retorna um [objeto DVDRect](dvdrect-object.md) que contém quatro propriedades de leitura/gravação: (superior esquerdo) x; (superior esquerdo) y, Width e Height. As **propriedades x** e **y** são definidas como zero e as outras duas propriedades refletem a largura e a altura do retângulo de vídeo, conforme criado no disco.

 

 



