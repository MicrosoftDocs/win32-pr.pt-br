---
description: O terminal do CAudioRenderTerminal é derivado de CSingleFilterTerminal e implementa um terminal de processamento de áudio estático para dispositivos de som wave usando o filtro de ondas do DirectShow. A maioria dos MSPs não precisará substituir a implementação desse terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757970"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

O terminal do **CAudioRenderTerminal** é derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de processamento de áudio estático para dispositivos de som wave usando o filtro de ondas do DirectShow. A maioria dos MSPs não precisará substituir a implementação desse terminal.

Definido em MSPtrmar. h.

## <a name="remarks"></a>Comentários

Os métodos de balanceamento [**Put \_**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**obter \_ balanceamento**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** não são implementados e retornarão e \_ NOTIMPL.

 

 



