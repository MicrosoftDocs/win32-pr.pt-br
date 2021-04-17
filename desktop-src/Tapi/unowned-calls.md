---
description: Para impedir que chamadas sem proprietário estejam no sistema de telefonia, a TAPI descartará chamadas que tenham sido sinalizadas de um provedor de serviços se não for possível identificar um aplicativo para ser o proprietário inicial da chamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chamadas sem proprietário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757195"
---
# <a name="unowned-calls"></a>Chamadas sem proprietário

Para impedir que chamadas sem proprietário estejam no sistema de telefonia, a TAPI descartará chamadas que tenham sido sinalizadas de um provedor de serviços se não for possível identificar um aplicativo para ser o proprietário inicial da chamada. Na TAPI versão 2,0 e posterior, a TAPI chama a função [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) para descartar a chamada.

O provedor de serviços pode saber com antecedência se há um aplicativo disponível para apropriar-se de uma nova chamada. A TAPI sempre informa ao provedor de serviços os tipos de mídia para os quais há um aplicativo disponível usando a função [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .

Por exemplo, se um provedor de serviços determinar que há uma chamada ativa na linha que tem o \_ modo LINEMEDIAMODE INTERACTIVEVOICE, ele deverá verificar a detecção de mídia padrão antes de gerar as mensagens [**\_ NewCall de linha**](line-newcall.md) e [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) . Se a detecção de mídia padrão mostrar que nenhum aplicativo está procurando uma \_ chamada LINEMEDIAMODE INTERACTIVEVOICE, o provedor de serviços não deverá enviar as mensagens, pois a TAPI a removerá imediatamente.

 

 
