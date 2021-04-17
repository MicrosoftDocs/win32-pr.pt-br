---
description: Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest2:: RequestComputeShaderDataAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812342"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>Método IPipeLineStagesRequest2:: RequestComputeShaderDataAsync

Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*1008*   
O evento de expedição especificado.

*requestCallback*   
O endereço do retorno de chamada usado para notificar o host dos resultados.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Consulte também

[**IPipeLineStagesRequest2**](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
