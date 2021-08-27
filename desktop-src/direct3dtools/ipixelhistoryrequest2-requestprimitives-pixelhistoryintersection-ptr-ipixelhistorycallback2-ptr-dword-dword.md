---
description: Solicita uma lista de primitivos de uma interseção específica. Para obter mais informações, consulte a função membro RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPixelHistoryRequest2::RequestPrimitives
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4ce4398daac6e13d90624499c83f451c12602d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626622"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>Método IPixelHistoryRequest2::RequestPrimitives

Solicita uma lista de primitivos de uma interseção específica. Para obter mais informações, consulte a função membro RequestIntersections.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*Interseção*   
O endereço da interseção especificada.

*requestCallback*   
O endereço do retorno de chamada usado para notificar o host de resultados.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixelHistoryRequest2**](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
