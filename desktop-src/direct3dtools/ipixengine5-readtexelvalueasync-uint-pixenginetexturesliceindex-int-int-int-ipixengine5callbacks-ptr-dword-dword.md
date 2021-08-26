---
description: Lê um valor de texel e retorna o resultado para o host de forma assíncrona.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPixEngine5::ReadTexelValueAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c8b7a5db59da4160f870e9e2c7bc1ac3701432e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627412"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5::ReadTexelValueAsync

Lê um valor de texel e retorna o resultado para o host de forma assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*textureId*   
A ID da textura da onde ler o valor de texel.

*sliceIndex*   
O índice da fatia dentro da textura da onde ler o valor de texel.

*X*   
A coordenada x texel a ser lida.

*Y*   
A coordenada y texel a ser lida.

*formatOverride*   
A substituição de formato de cor.

*Retornos*   
O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
