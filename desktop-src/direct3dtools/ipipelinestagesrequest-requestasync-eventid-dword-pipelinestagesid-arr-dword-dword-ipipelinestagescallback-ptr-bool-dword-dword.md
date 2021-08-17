---
description: Uma solicitação assíncrona para obter imagens de visualização para a janela de estágios do pipeline de gráficos.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPipeLineStagesRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 890e0d95e811b47582a46ca0a1bc7a66dcbbb3fa5e6dab8a15d9e886730f22ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721773"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Método IPipeLineStagesRequest::RequestAsync

Uma solicitação assíncrona para obter imagens de visualização para a janela de estágios do pipeline de gráficos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*Eventid*   
A ID do evento gráfico para o que as imagens estão sendo solicitadas.

*numStages*   
O número de estágios de pipeline para os que as imagens estão sendo solicitadas.

*count1 \_ stageIds*   
IDs dos estágios de pipeline para os que as imagens estão sendo solicitadas.

*Largura*   
A largura das imagens solicitadas.

*Altura*   
A altura das imagens solicitadas.

*requestCallback*   
O endereço do retorno de chamada usado para notificar o host dos resultados.

*getMeshData*   
true para retornar dados de malha; caso contrário, false.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPipeLineStagesRequest**](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
