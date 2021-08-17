---
description: Um retorno de chamada que notifica o host de quais estágios de pipeline não podem retornar dados de malha para o evento especificado na solicitação associada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: MeshDataNotAvailableCallback'
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
ms.openlocfilehash: 41fbedaa6deaf2a799f8d721309bfbe1b44bc2110dfae0a3cf30a4afbe0fa1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276076"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Método IPipeLineStagesCallback:: MeshDataNotAvailableCallback

Um retorno de chamada que notifica o host de quais estágios de pipeline não podem retornar dados de malha para o evento especificado na solicitação associada.

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

*erros de count0 \_*   
Os erros de estágio do pipeline.

*Largura*   
A largura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização do pipeline.

*tamanho*   
A altura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização do pipeline.

*Eid*   
O evento representado nos resultados.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
