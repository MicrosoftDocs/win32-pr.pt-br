---
description: Retorno de chamada do mecanismo que indica que é concluído a análise de todos os novos quadros adicionados ao log.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f9d47e84cf4deeebafa6592853f73e86d8339f8
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787312"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>Interface INewFramesCallback

Retorno de chamada do mecanismo que indica que é concluído a análise de todos os novos quadros adicionados ao log.

## <a name="members"></a>Membros

A interface **INewFramesCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INewFramesCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **INewFramesCallback** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descrição</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td ><p>Um retorno de chamada que notifica o host de que todas as solicitações foram canceladas.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de uma solicitação cancelada.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td ><p>Um retorno de chamada que notifica o host de uma solicitação cancelada usando um cookie que identifica exclusivamente a solicitação.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td ><p>Um retorno de chamada que notifica o host que novos quadros estão disponíveis para serem processados.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
