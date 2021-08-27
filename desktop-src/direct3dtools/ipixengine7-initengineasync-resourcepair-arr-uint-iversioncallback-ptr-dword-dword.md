---
description: O passa os recursos de forma assíncrona para o mecanismo, como cadeias de caracteres para mensagens de erro.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine7:: InitEngineAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 45bd2b6de1e810a8550be844f44eba22208e0b58
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623372"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>Método IPixEngine7:: InitEngineAsync

O passa os recursos de forma assíncrona para o mecanismo, como cadeias de caracteres para mensagens de erro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*recursos do count1 \_*   
Uma matriz de recursos.

*contar*   
O número de recursos em \_ recursos count1

*versionCallback*   
O endereço do retorno de chamada usado para notificar o host dos resultados.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine7**](/windows/desktop/direct3dtools/ipixengine7)

 

 
