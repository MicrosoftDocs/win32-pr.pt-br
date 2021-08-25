---
description: Para impedir que chamadas sem proprietário sejam no sistema de telefonia, a TAPI descarta chamadas que foram sinalizadas de um provedor de serviços se não puder identificar um aplicativo como o proprietário inicial da chamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chamadas sem proprietário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea6fffa2ee65f24d73337980e2a8952157aa5d1000e5c657d75af372f26f00d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991646"
---
# <a name="unowned-calls"></a>Chamadas sem proprietário

Para impedir que chamadas sem proprietário sejam no sistema de telefonia, a TAPI descarta chamadas que foram sinalizadas de um provedor de serviços se não puder identificar um aplicativo como o proprietário inicial da chamada. No TAPI versão 2.0 e posterior, TAPI chama a [**função TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) para soltar a chamada.

O provedor de serviços pode saber com antecedência se há ou não um aplicativo disponível para assumir a propriedade de uma nova chamada. A TAPI sempre informa o provedor de serviços dos tipos de mídia para os quais há um aplicativo disponível usando a [**função TSPI \_ lineSetDefaultMediaDetection.**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)

Por exemplo, se um provedor de serviços determinar que há uma chamada ativa na linha com o modo LINEMEDIAMODE INTERACTIVEVOICE, ele deverá verificar a detecção de mídia padrão antes de gerar as mensagens \_ [**LINE \_ NEWCALL**](line-newcall.md) e [**LINE \_ CALLSTATE.**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Se a detecção de mídia padrão mostrar que nenhum aplicativo está procurando uma chamada LINEMEDIAMODE INTERACTIVEVOICE, o provedor de serviços não deverá enviar as mensagens, pois a TAPI a \_ soltará imediatamente.

 

 
