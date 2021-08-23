---
description: O método IsUsingDefaultSource determina se o renderizador está usando a janela de origem padrão.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Método CBaseControlVideo. IsUsingDefaultSource (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dce06ffa85b3736eca17f1ecb8303a41afb142fcc8b0d369e1f264a0cf47b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955205"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>Método CBaseControlVideo. IsUsingDefaultSource

O `IsUsingDefaultSource` método determina se o renderizador está usando a janela de origem padrão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o renderizador estiver usando a origem padrão; caso contrário, retornará S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




