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
# <a name="caudiorenderterminal"></a><span data-ttu-id="13498-104">CAudioRenderTerminal</span><span class="sxs-lookup"><span data-stu-id="13498-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="13498-105">O terminal do **CAudioRenderTerminal** é derivado de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa um terminal de processamento de áudio estático para dispositivos de som wave usando o filtro de ondas do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="13498-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="13498-106">A maioria dos MSPs não precisará substituir a implementação desse terminal.</span><span class="sxs-lookup"><span data-stu-id="13498-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="13498-107">Definido em MSPtrmar. h.</span><span class="sxs-lookup"><span data-stu-id="13498-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="13498-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="13498-108">Remarks</span></span>

<span data-ttu-id="13498-109">Os métodos de balanceamento [**Put \_**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**obter \_ balanceamento**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** não são implementados e retornarão e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="13498-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



