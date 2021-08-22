---
description: Solicitações para iniciar uma sessão de depuração de sombreador para o estágio de pipeline especificado, pixel/vértice, se aplicável, evento e quadro.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IDebugShaderRequest:: BeginDebugShader'
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
ms.openlocfilehash: e84a0f76f360340bb9a4ddffa6ecf5ad72bf8de8d4510b4129e3c6ab618b516a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406222"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Método IDebugShaderRequest:: BeginDebugShader

Solicitações para iniciar uma sessão de depuração de sombreador para o estágio de pipeline especificado, pixel/vértice, se aplicável, evento e quadro.

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

*1008*   
O evento especificado.

*frameNumber*   
O quadro especificado.

*deles*   
O vértice especificado. Aplica-se somente ao depurar um sombreador de vértice.

*16x16*   
O pixel especificado. Aplica-se somente ao depurar um sombreador de pixel.

*Test*   
O estágio de pipeline especificado.

*pPixelHistory*   
O endereço dos resultados do histórico de pixel usado para localizar o pixel associado a ser depurado. Aplica-se somente ao depurar um sombreador de pixel.

*pDevice*   
O endereço a ser passado para o mecanismo de depuração para comunicação com esta sessão de depuração (ReadProcessMemory do mecanismo de depuração neste endereço).

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
