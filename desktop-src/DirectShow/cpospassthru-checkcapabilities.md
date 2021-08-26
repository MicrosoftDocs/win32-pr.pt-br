---
description: 'O método CheckCapabilities consulta se um fluxo especificou recursos de busca. Esse método implementa o método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Método CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108416"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Método CPosPassThru. CheckCapabilities

O `CheckCapabilities` método consulta se um fluxo especificou recursos de busca. Esse método implementa o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Ponteiro para uma combinação de bits de um ou mais atributos de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) em busca. Quando o método retorna, o valor indica quais desses atributos estão disponíveis.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




