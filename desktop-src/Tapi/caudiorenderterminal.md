---
description: o terminal CAudioRenderTerminal é derivado de CSingleFilterTerminal e implementa um terminal de processamento de áudio estático para dispositivos wave usando o filtro de DirectShow waveout. A maioria dos MSPs não precisará substituir a implementação desse terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1baaa4a2d1e5d7bbe3b72de19de8593be8976ed662e27595dccea4b7432daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869811"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

o terminal **CAudioRenderTerminal** é derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de processamento de áudio estático para dispositivos wave usando o filtro de DirectShow waveout. A maioria dos MSPs não precisará substituir a implementação desse terminal.

Definido em MSPtrmar. h.

## <a name="remarks"></a>Comentários

Os métodos de balanceamento [**Put \_**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**obter \_ balanceamento**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** não são implementados e retornarão e \_ NOTIMPL.

 

 



