---
description: Um retorno de chamada que notifica o host das informações de interseção do histórico de pixel retornado pela solicitação assocaited.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryCallback2:: IntersectionsCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087547"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>Método IPixelHistoryCallback2:: IntersectionsCallback

Um retorno de chamada que notifica o host das informações de interseção do histórico de pixel retornado pela solicitação assocaited.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a>Parâmetros

*contar*   
O número de interseções de histórico de pixel.

*interseções count0 \_*   
As interseções de histórico de pixel.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Consulte também

[**IPixelHistoryCallback2**](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
