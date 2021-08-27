---
description: Uma solicitação assíncrona para obter os arquivos de origem associados ao callstack de um evento.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método ISourceFileInfoRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: af2b1b924bd10afce3172ec0119c864fe4f7349c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624152"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Método ISourceFileInfoRequest::RequestAsync

Uma solicitação assíncrona para obter os arquivos de origem associados ao callstack de um evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*Eventid*   
O evento especificado.

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

[**ISourceFileInfoRequest**](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
