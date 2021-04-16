---
description: Um retorno de chamada que notifica o host do pipeline prepara as informações de malha retornadas pela solicitação assocaited.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: MeshDataVertCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500384"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Método IPipeLineStagesCallback:: MeshDataVertCallback

Um retorno de chamada que notifica o host do pipeline prepara as informações de malha retornadas pela solicitação assocaited.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Parâmetros

*numVertices*   
O número de vértices nos resultados.

*numBufferLayoutEntries*   
O número de entradas de layout de buffer nos resultados.

*entradas de count1 \_*   
O layout do buffer é todo. Elas descrevem a assinatura de saída do sombreador.

*Stride*   
O tamanho (STRIDE) de uma parte de saída inteira.

*numVBBytes*   
O tamanho do buffer de vértice em bytes.

*count4 \_ pVBData*   
O buffer de vértice.

*numIBBytes*   
O tamanho do buffer de índice em bytes.

*count6 \_ pIBData*   
O buffer de índice.

*indexSize*   
O tamanho de cada índice em bytes.

*IBOffset*   
Um deslocamento no buffer de índice que especifica onde os índices devem começar a ser usados.

*baseVertex*   
Um deslocamento para o buffer de vértice que especifica onde os vértices devem começar a ser usados.

*minVertex*   

*IBIndexesVB*   
verdadeiro quando o buffer de índice é usado; caso contrário, false.

*numIndices*   
O número de índices usados.

*visualização*   
O topolology do sombreador. Isso não é necessariamente o mesmo que a topologia da chamada Draw associada.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
