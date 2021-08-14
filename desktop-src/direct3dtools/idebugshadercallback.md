---
description: Retorno de chamada para retornar as instruções geradas da criação de um rastreamento de sombreador.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IDebugShaderCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf11c453ccf1d9431e5273ec909015de5916ff3faccc0c3d06d1cb8d29073870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981576"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span id="vspixengine.idebugshadercallback"></span>Interface IDebugShaderCallback

Retorno de chamada para retornar as instruções geradas da criação de um rastreamento de sombreador.

## <a name="members"></a>Membros

A interface **IDebugShaderCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDebugShaderCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **IDebugShaderCallback** tem esses métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descrição</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></td><td style="text-align: left;"><p>Um retorno de chamada que notifica o host das informações de instructrion retornadas pela solicitação associada.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
