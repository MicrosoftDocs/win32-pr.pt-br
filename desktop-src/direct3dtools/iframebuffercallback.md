---
description: Retorno de chamada para retornar um destino de renderização. O formato do destino de renderização retornado é R8G8B8A8 \_ UNORM, independentemente do formato do renderTarget in-Engine.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 479796ebf225ceac4e93f429aa6b8412e3f86398
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628834"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>Interface IFrameBufferCallback

Retorno de chamada para retornar um destino de renderização. O formato do destino de renderização retornado é R8G8B8A8 \_ UNORM, independentemente do formato do renderTarget in-Engine.

## <a name="members"></a>Membros

A interface **IFrameBufferCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IFrameBufferCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Maneiras

A interface **IFrameBufferCallback** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descrição</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
