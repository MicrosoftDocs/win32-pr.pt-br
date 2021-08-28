---
description: Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameBufferCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2308ec5355da8f8fda7eeccf31d1cbe19e8a8247
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626672"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Método IFrameBufferCallback:: ResultCallback

Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Parâmetros

*frameNumber*   
O número do quadro.

*Largura*   
A largura do quadro.

*tamanho*   
A altura do quadro.

*renderTargetPtr*   
O destino de renderização do qual os resultados são provenientes. É sempre um slot especificado pela solicitação de buffer de quadro ou, se não for uma chamada de desenho, então o primeiro RTV Bount à fonte de saída.

*frameDuraction*   
Não usado.

*tamanho*   
O tamanho do buffer de saída em bytes.

*\_buffer count5*   
O conteúdo do destino de renderização no \_ formato R8G8B8A8 UNORM.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
