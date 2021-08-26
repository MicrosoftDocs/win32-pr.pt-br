---
description: Método CSourceSeeking.GetCapabilities – o método GetCapabilities recupera todos os recursos de busca do fluxo. Esse método implementa o método IMediaSeeking::GetCapabilities.
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Método CSourceSeeking.GetCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96e3a637673a91ebc98e48777b8f42bdcbf02654a0c264037a66b4121f5b80ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054336"
---
# <a name="csourceseekinggetcapabilities-method"></a>Método CSourceSeeking.GetCapabilities

O `GetCapabilities` método recupera todos os recursos de busca do fluxo. Esse método implementa o [**método IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pcapabilities* 
</dt> <dd>

Ponteiro para uma variável que recebe uma combinação bit a bit de [**sinalizadores AM \_ SEEKING SEEKING \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | **Valor do** ponteiro NULL<br/> |



 

## <a name="remarks"></a>Comentários

Os recursos de busca são especificados pela variável de membro [**CSourceSeeking::m \_ dwSeekingCaps.**](csourceseeking-m-dwseekingcaps.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




