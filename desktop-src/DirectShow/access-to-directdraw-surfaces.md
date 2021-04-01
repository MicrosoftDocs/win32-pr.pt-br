---
description: Acesso a superfícies do DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Acesso a superfícies do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825994"
---
# <a name="access-to-directdraw-surfaces"></a>Acesso a superfícies do DirectDraw

Os objetos de exemplo de mídia fornecidos pelo VMR para filtros upstream dão suporte à interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Para obter a interface, chame QueryInterface na interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e especifique IID \_ IVMRSurface. Os filtros upstream podem usar os métodos IVMRSurface para acessar e manipular a superfície que foi criada pelo VMR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o VMR para desenvolvedores de filtro do DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



