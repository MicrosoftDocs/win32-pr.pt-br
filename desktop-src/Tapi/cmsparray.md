---
description: O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921830"
---
# <a name="cmsparray"></a>CMSPArray

O modelo CMSPArray implementa uma matriz inteligente que aumentará sob demanda. Ele foi projetado para manter pequenas matrizes com tipos de dados simples. Ele não tem uma seção crítica. Suas únicas dependências são **realloc** e **memmove**. Ele é usado internamente para manter listas de ponteiros de objeto. É semelhante à implementação de **CSimpleArray** da ATL, mas é mais eficiente para alocações iniciais.

Esse modelo é definido em MSPutils. h.

 

 



