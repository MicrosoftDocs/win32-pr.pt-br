---
description: Uma enumeração usada para indicar por que um pixel foi rejeitado.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296013"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumeração PIXELKILLREASON

Uma enumeração usada para indicar por que um pixel foi rejeitado.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ nenhum**  
Um valor que indica que o pixel não foi rejeitado.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Um valor que indica que o pixel foi rejeitado porque o sombreador não foi executado.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Um valor que indica que o pixel foi rejeitado porque houve falha no teste de tesoura.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Um valor que indica que o pixel foi rejeitado porque o teste alfa falhou.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de estêncil falhou.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de profundidade falhou.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Um valor que indica que o histórico de pixels não pode ser computado.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**erro de PKR \_**  
Um valor que indica que o pixel foi rejeitado devido a um erro geral.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR sem \_ INTERseção**  
Um valor que indica que o pixel foi rejeitado porque a chamada de desenho não cruza o pixel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ obstruído**  
Um valor que indica que o pixel foi rejeitado porque o desenho foi obstruído.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Um valor que indica que o pixel foi rejeitado porque a profundidade e o teste de estêncil falharam.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



