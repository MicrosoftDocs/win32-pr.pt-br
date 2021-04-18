---
description: Representa informações sobre um específico.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760640"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>Estrutura PixelHistoryIntersection

Representa informações sobre um determinado

## <a name="syntax"></a>Sintaxe


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Membros

**frameNumber**  
O quadro do evento de gráficos assocaited com esta operação.

**Eid**  
A ID do evento de gráficos associado a esta operação.

**renderTargetPtr**  
O destino de renderização originalmente associado (dentro do aplicativo capturado) com esta operação.

**eventType**  
O tipo de evento associado a essa operação (especificamente, se esse evento é uma chamada de desenho).

**empresas**  
As coordenadas do pixel no framebuffer.

**bAssemblerStageGeneratesInstanceID**  
true se o montador de entrada gerar IDs de instância; caso contrário, false.

**sinalizadores**  
Uma combinação de valores PIXELHISTORYFLAGS. Para obter mais informações, consulte a enumeração PIXELHISTORYFLAGS.

**fbInitialRed**  
Framebuffer: valor do componente de cor vermelha de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.

**fbInitialGreen**  
Framebuffer: valor do componente de cor verde de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.

**fbInitialBlue**  
Framebuffer: valor do componente de cor azul de framebuffer antes de qualquer saída de sombreador de pixel ser mesclada; ou seja, no início deste quadro.

**fbInitialAlpha**  
Framebuffer: o valor do componente de cor alfa de framebuffer antes que qualquer saída de sombreador de pixel seja mesclada; ou seja, no início deste quadro.

**LabelFBInitialRed**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.

**LabelFBInitialGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.

**LabelFBInitialBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.

**LabelFBInitialAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer antes de qualquer sombreamento de pixel; ou seja, no início deste quadro.

**fbRed**  
Framebuffer: valor do componente de cor vermelha de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.

**fbGreen**  
Framebuffer: valor do componente de cor verde de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.

**fbBlue**  
Framebuffer: valor do componente de cor azul de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.

**fbAlpha**  
Framebuffer: o valor do componente de cor alfa de framebuffer depois que a saída do sombreador de pixel é mesclada; ou seja, a cor final do framebuffer.

**LabelFBRed**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor vermelha do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.

**LabelFBGreen**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor verde do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.

**LabelFBBlue**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor azul do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.

**LabelFBAlpha**  
Uma cadeia de caracteres COM que contém o nome do rótulo associado ao componente de cor alfa do framebuffer após todo o sombreamento de pixel; ou seja, a cor final do framebuffer.

**pixelKillReason**  
Especifica o motivo pelo qual a contribuição de cores do pixel foi interrompida.

**Resultado**  
Se ocorreu um erro, contém o HRESULT do DirectX que especifica o erro.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



