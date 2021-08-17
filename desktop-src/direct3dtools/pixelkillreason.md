---
description: Uma enum usada para indicar por que um pixel foi rejeitado.
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
ms.openlocfilehash: 58ead08f81c8dee1644e431ae100c5100551e9907ab9a9d5bf00f6aae3532abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119320"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumeração PIXELKILLREASON

Uma enum usada para indicar por que um pixel foi rejeitado.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ NONE**  
Um valor que indica que o pixel não foi rejeitado.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**SOMBREADOR \_ PKRKILL**  
Um valor que indica que o pixel foi rejeitado porque o sombreador não foi executado.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de tesoura falhou.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Um valor que indica que o pixel foi rejeitado porque o teste alfa falhou.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de estêncil falhou.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de profundidade falhou.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Um valor que indica que o histórico de pixels não pode ser computado.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**ERRO \_ PKR**  
Um valor que indica que o pixel foi rejeitado devido a um erro geral.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**  
Um valor que indica que o pixel foi rejeitado porque a chamada de desenho não intersecção do pixel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ OCCLUDED**  
Um valor que indica que o pixel foi rejeitado porque o desenho foi ocluído.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Um valor que indica que o pixel foi rejeitado porque o teste de profundidade e estêncil falhou.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



