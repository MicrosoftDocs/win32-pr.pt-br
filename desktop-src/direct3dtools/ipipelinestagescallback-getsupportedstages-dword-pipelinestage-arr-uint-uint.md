---
description: Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPipeLineStagesCallback::GetSupportedStages
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91e2d80813d8d87c92819aab29dbc368b397d074
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623302"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Método IPipeLineStagesCallback::GetSupportedStages

Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a>Parâmetros

*numColumns*   
O número de estágios retornados.

*count0 \_ pStages*   
Os estágios do pipeline.

*swapChainWidth*   
A largura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização de pipeline.

*swapChainHeight*   
A altura da cadeia de permuta assocaited com a chamada de desenho. Isso é usado ao solicitar imagens de visualização de pipeline.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
