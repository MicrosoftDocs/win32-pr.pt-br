---
description: O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682105bee8b39235c36865b6349d9519f16d42ff97844815a85f438f9983eb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869118"
---
# <a name="cmsparray"></a>CMSPArray

O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda. Ele foi projetado para manter pequenas matrizes com tipos de dados simples. Ele não tem uma seção crítica. Suas únicas dependências são **realloc** e **memmove**. Ele é usado internamente para manter listas de ponteiros de objeto. É semelhante à implementação de **CSimpleArray** da ATL, mas é mais eficiente para alocações iniciais.

Esse modelo é definido em MSPutils. h.

 

 



