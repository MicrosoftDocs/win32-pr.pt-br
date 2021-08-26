---
description: Solicitações para obter o conteúdo bruto de um bloco.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ITileRequest:: RequestBufferTileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fe9b93e5762942d26325df0816a08d0a4d2101e8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624742"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Método ITileRequest:: RequestBufferTileAsync

Solicitações para obter o conteúdo bruto de um bloco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*1008*   
O evento especificado para corresponder o conteúdo do bloco a (por exemplo, um destino de renderização pode mudar ao longo do tempo).

*RequestedDataUID*   
O endereço do bloco especificado.

*Grupo*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os resultados são gravados.

*tileIndex*   
O índice do bloco especificado.

*requestCallback*   
O endereço do retorno de chamada usado para notificar o host dos resultados.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método tiver sucesso, ele retornará **S_OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**ITileRequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
