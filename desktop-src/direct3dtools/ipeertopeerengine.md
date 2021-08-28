---
description: Interface para comunicação remota de dados sobre um vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e654d7dd31aa003dbd97af9cafb6831e914f2f7
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623312"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span id="vspixengine.ipeertopeerengine"></span>Interface IPeerToPeerEngine

Interface para comunicação remota de dados sobre um vsglog.

## <a name="members"></a>Membros

A interface **IPeerToPeerEngine** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPeerToPeerEngine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **IPeerToPeerEngine** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descrição</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Cancela uma solicitação anterior para configurar uma conexão remota.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Obtém o endereço do ponto de extremidade de um mecanismo remoto.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Define o endereço do ponto de extremidade usado para se conectar a um mecanismo remoto.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
