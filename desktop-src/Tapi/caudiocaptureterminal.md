---
description: O terminal CAudioCaptureTerminal é derivado de CSingleFilterTerminal e implementa um terminal de captura de áudio estático para dispositivos Wave usando o filtro Wave do DirectShow. A maioria dos MSPs não precisará substituir a implementação desse terminal.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781053"
---
# <a name="caudiocaptureterminal"></a>CAudioCaptureTerminal

O terminal **CAudioCaptureTerminal** é derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de captura de áudio estático para dispositivos Wave usando o filtro Wave do DirectShow. A maioria dos MSPs não precisará substituir a implementação desse terminal.

Definido em MSPtmac. h.

## <a name="remarks"></a>Comentários

Os métodos de balanceamento [**Put \_**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**obter \_ balanceamento**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** não são implementados e retornarão e \_ NOTIMPL.

 

 



