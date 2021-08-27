---
description: Uma função de retorno de chamada usada para notificar o host de resultados de uma ação (por exemplo, capturar um quadro) que ela solicitou.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IRunActionCallback::RequestResult
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e806a95515a59176c1070b573763a8581f40397
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627552"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>Método IRunActionCallback::RequestResult

Uma função de retorno de chamada usada para notificar o host de resultados de uma ação (por exemplo, capturar um quadro) que ela solicitou.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a>Parâmetros

*Actionresult*   
O resultado da ação.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IRunActionCallback**](/windows/desktop/direct3dtools/irunactioncallback)

 

 
