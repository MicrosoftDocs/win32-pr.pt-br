---
description: A lista a seguir contém os métodos públicos CMSPCallMultiGraph chamados pelo pool de threads.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Métodos públicos CMSPCallMultiGraph, chamados pelo pool de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757000"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>Métodos públicos CMSPCallMultiGraph, chamados pelo pool de threads



| Métodos públicos CMSPCallMultiGraph                                   | Descrição                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | Chamado quando o grafo de filtro sinaliza um evento.                                                                                                                                                           |
| [**HandleGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | Chamado pelo método estático [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) . Enfileira [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) no thread de trabalho principal do MSP. |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | Permite que a instância do objeto de chamada MSP manipule o evento Filter Graph.                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



