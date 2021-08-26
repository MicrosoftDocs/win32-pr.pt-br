---
title: Fluxos de Script em DirectShow
description: Fluxos de Script em DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows SDK do formato de mídia, DirectShow
- Windows SDK do formato de mídia, fluxos de script
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- DirectShow, fluxos de script
- fluxos de script, DirectShow
- fluxos, fluxos de script em DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929615"
---
# <a name="script-streams-in-directshow"></a>Fluxos de Script em DirectShow

quando o filtro de leitor ASF do WM recebe um arquivo que inclui um fluxo do tipo \_ script WMMEDIATYPE, ele cria um pino de saída para ele que pode ser conectado ao filtro de processador de comando de Script interno DirectShow. Quando você chama **IGraphBuilder:: RenderFile**, esse filtro é adicionado automaticamente ao grafo e conectado. Quando o renderizador de comando de script interno recebe um exemplo contendo um comando de script, ele dispara um **\_ \_ evento OLE do EC** cujo **lParam** contém o script. O aplicativo é totalmente responsável por manipular esse evento. para obter mais informações sobre o **\_ \_ evento OLE do EC**, consulte a documentação do SDK do DirectShow.

 

 




