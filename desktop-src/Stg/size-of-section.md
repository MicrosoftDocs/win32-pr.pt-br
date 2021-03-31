---
title: Tamanho da seção
description: O tipo de dados de tamanho da seção indica o tamanho, em bytes, da seção.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160382"
---
# <a name="size-of-section"></a>Tamanho da seção

O tipo de dados de tamanho da seção indica o tamanho, em bytes, da seção. Como o tamanho da seção é dos primeiros 4 bytes, as seções podem ser copiadas como uma matriz de bytes. O tamanho da seção deve ser sempre um múltiplo de quatro.

Por exemplo, uma seção vazia, ou seja, uma com zero propriedades, teria uma contagem de bytes de oito (a contagem de bytes **DWORD** e a contagem de propriedades **DWORD** ). A seção em si conterá os 8 bytes: **08 00 00 00 00 00 00 00**.

 

 




