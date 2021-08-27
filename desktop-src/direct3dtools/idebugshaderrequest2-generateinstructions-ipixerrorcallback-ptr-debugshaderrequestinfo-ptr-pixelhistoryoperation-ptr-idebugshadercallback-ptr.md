---
description: Solicitações para gerar instruções de rastreamento do sombreador em uma solicitação de depuração. A depuração baseada em rastreamento ocorre na CPU (distorção) em vez da GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IDebugShaderRequest2::GenerateInstructions
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3af0e624435c03416db0bf8d74bc3aa8418ae78
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625152"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Método IDebugShaderRequest2::GenerateInstructions

Solicitações para gerar instruções de rastreamento do sombreador em uma solicitação de depuração. A depuração baseada em rastreamento ocorre na CPU (distorção) em vez da GPU.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Parâmetros

*errorCallback*   
O endereço de um retorno de chamada para erros que podem ocorrer durante a geração de instruções de rastreamento do sombreador.

*Requestinfo*   
O endereço de uma estrutura DebugShaderRequestInfo que descreve o evento/vértice/pixel solicitado.

*pPixelHistory*   
O endereço dos resultados do histórico de pixels usado para localizar o pixel associado a ser depurado. Aplica-se somente ao depurar um sombreador de pixel.

*Pcallback*   
O endereço de um retorno de chamada usado para notificar o host dos resultados.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
