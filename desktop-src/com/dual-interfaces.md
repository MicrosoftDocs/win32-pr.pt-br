---
title: Interfaces duplas (COM)
description: Interfaces duplas
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008476"
---
# <a name="dual-interfaces"></a>Interfaces duplas

A automação OLE permite que um objeto exponha um conjunto de métodos de duas maneiras: por meio da interface **IDispatch** e por meio da associação direta de OLE vtable. O **IDispatch** é usado pela maioria das ferramentas disponíveis hoje e oferece suporte para associação tardia a propriedades e métodos.

A associação VTable oferece um desempenho muito maior porque esse método é chamado diretamente, em vez de **IDispatch:: Invoke**. O **IDispatch** oferece suporte de associação tardia, em que a ligação Direct vtable oferece um lucro significativo de desempenho; ambas as técnicas são valiosas e importantes em cenários diferentes. Ao rotular uma interface como \[ [**dupla**](/windows/desktop/Midl/dual) \] na biblioteca de tipos, uma interface de automação OLE pode ser usada por meio de **IDispatch** ou pode ser associada diretamente. Os contêineres podem, portanto, escolher a técnica mais apropriada. O suporte para interfaces duplas é altamente recomendável para controles e contêineres.

 

 