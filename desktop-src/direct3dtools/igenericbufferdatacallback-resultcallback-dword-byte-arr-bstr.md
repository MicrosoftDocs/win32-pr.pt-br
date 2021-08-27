---
description: Um retorno de chamada que notifica o host de informações de buffer genéricas retornadas pela solicitação assocaited.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IGenericBufferDataCallback::ResultCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0035b0546b863c87c54fbd09bbc62897ab581bfe
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622322"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Método IGenericBufferDataCallback::ResultCallback

Um retorno de chamada que notifica o host de informações de buffer genéricas retornadas pela solicitação assocaited.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a>Parâmetros

*Tamanho*   
O tamanho do conteúdo do buffer em bytes.

*count0 \_ buffer*   
O conteúdo do buffer. Na maioria dos casos, são dados XML.

*Tipo*   
Uma cadeia de caracteres COM que indica o tipo de conteúdo retornado no buffer.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IGenericBufferDataCallback**](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
