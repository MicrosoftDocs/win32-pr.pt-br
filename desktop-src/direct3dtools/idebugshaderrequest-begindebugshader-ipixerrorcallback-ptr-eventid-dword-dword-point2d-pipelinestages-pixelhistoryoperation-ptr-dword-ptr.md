---
description: Solicita para iniciar uma sessão de depuração de sombreador para o estágio de pipeline, pixel/vértice especificado, se aplicável, evento e quadro.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IDebugShaderRequest::BeginDebugShader
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629850"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Método IDebugShaderRequest::BeginDebugShader

Solicita para iniciar uma sessão de depuração de sombreador para o estágio de pipeline, pixel/vértice especificado, se aplicável, evento e quadro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Parâmetros

*errorCallback*   
O endereço de um retorno de chamada para erros que podem ocorrer durante a depuração.

*Eventid*   
O evento especificado.

*frameNumber*   
O quadro especificado.

*Vértice*   
O vértice especificado. Aplica-se somente ao depurar um sombreador de vértice.

*Pixel*   
O pixel especificado. Aplica-se somente ao depurar um sombreador de pixel.

*Palco*   
O estágio de pipeline especificado.

*pPixelHistory*   
O endereço dos resultados do histórico de pixels usado para localizar o pixel associado a ser depurado. Aplica-se somente ao depurar um sombreador de pixel.

*pDevice*   
O endereço a ser aprovado para o mecanismo de depuração para se comunicar com essa sessão de depuração (readprocessmemory do mecanismo de depuração nesse endereço).

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
