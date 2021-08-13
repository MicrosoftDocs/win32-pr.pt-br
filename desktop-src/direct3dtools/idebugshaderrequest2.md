---
description: 'Solicitação para iniciar a depuração de um sombreador. Essa solicitação contém duas partes: gerar um rastreamento e depurar um rastreamento.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b508cd8f8e4dfb98f3a4cfd758599affb2bdfaf05fb97afe9fbeac8e18e4b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283735"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span id="vspixengine.idebugshaderrequest2"></span>Interface IDebugShaderRequest2

Solicitação para iniciar a depuração de um sombreador. Essa solicitação contém duas partes: gerar um rastreamento e depurar um rastreamento.

## <a name="members"></a>Membros

A interface **IDebugShaderRequest2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDebugShaderRequest2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **IDebugShaderRequest2** tem esses métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descrição</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></td><td style="text-align: left;"><p>Solicitações para iniciar a depuração da lista de instruções especificada.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></td><td style="text-align: left;"><p>Solicitações para gerar instruções de rastreamento de sombreador em uma solicitação de depuração. A depuração baseada em rastreamento ocorre na CPU (Warp) em vez da GPU.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
