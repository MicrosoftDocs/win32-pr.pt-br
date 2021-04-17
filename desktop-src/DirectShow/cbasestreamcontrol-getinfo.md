---
description: 'O método GetInfo recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada. Esse método implementa o método IAMStreamControl:: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Método CBaseStreamControl. GetInfo (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757036"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Método CBaseStreamControl. GetInfo

O `GetInfo` método recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada. Esse método implementa o método [**IAMStreamControl:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações de fluxo am**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , alocada pelo chamador, que recebe as configurações de controle de fluxo atuais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




