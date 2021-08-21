---
description: O método GetInfo recupera informações sobre as configurações atuais de controle de fluxo, incluindo os horários de início e de parada. Esse método implementa o método IAMStreamControl::GetInfo.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Método CBaseStreamControl.GetInfo (Strmctl.h)
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
ms.openlocfilehash: 96bc59b6dc55d73aa16b08f53f831428ae2d2fb7b181d3bb255b61a323b236a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157213"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Método CBaseStreamControl.GetInfo

O `GetInfo` método recupera informações sobre as configurações atuais de controle de fluxo, incluindo os horários de início e de parada. Esse método implementa o [**método IAMStreamControl::GetInfo.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pinfo* 
</dt> <dd>

Ponteiro para uma [**estrutura AM \_ STREAM \_ INFO,**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) alocada pelo chamador, que recebe as configurações atuais de controle de fluxo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




