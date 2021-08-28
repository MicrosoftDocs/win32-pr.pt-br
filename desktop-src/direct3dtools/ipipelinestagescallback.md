---
description: <span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback – não usada. Anteriormente, um retorno de chamada para dados de estágios de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2fc828d902f1daa3b2c0c75d2f22671d9bdec942
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787491"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback

Não usado. Anteriormente, um retorno de chamada para dados de estágios de pipeline.

## <a name="members"></a>Membros

A interface **IPipeLineStagesCallback** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPipeLineStagesCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **IPipeLineStagesCallback** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descrição</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></td><td ><p>Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de quais estágios de pipeline não são capazes de retornar dados de malha para o evento especificado na solicitação associada.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de informações de malha de estágios de pipeline retornadas pela solicitação assocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>Resultcallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de informações de imagem de estágios de pipeline retornadas pela solicitação assocaited.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
