---
description: Um retorno de chamada que notifica o host de quais estágios de pipeline não são capazes de retornar dados de malha para o evento especificado na solicitação associada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPipeLineStagesCallback::MeshDataNotAvailableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622132"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Método IPipeLineStagesCallback::MeshDataNotAvailableCallback

Um retorno de chamada que notifica o host de quais estágios de pipeline não são capazes de retornar dados de malha para o evento especificado na solicitação associada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Parâmetros

*numberStages*   
O número de erros de estágio retornados.

*erros \_ count0*   
Os erros de estágio do pipeline.

*Largura*   
A largura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização de pipeline.

*Altura*   
A altura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização de pipeline.

*Eid*   
O evento representado nos resultados.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
