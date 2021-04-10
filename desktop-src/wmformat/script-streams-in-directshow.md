---
title: Fluxos de script no DirectShow
description: Fluxos de script no DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- DirectShow, fluxos de script
- fluxos de script, DirectShow
- fluxos, fluxos de script no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292732"
---
# <a name="script-streams-in-directshow"></a>Fluxos de script no DirectShow

Quando o filtro de leitor ASF do WM recebe um arquivo que inclui um fluxo do tipo \_ script WMMEDIATYPE, ele cria um pino de saída para ele que pode ser conectado ao filtro de processador de comandos de script interno do DirectShow. Quando você chama **IGraphBuilder:: RenderFile**, esse filtro é adicionado automaticamente ao grafo e conectado. Quando o renderizador de comando de script interno recebe um exemplo contendo um comando de script, ele dispara um **\_ \_ evento OLE do EC** cujo **lParam** contém o script. O aplicativo é totalmente responsável por manipular esse evento. Para obter mais informações sobre o **\_ \_ evento OLE do EC**, consulte a documentação do SDK do DirectShow.

 

 




