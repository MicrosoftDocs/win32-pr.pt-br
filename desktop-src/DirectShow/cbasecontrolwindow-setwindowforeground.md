---
description: O método SetWindowForeground move a janela de vídeo para o primeiro plano e, opcionalmente, dá o foco.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Método CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752521"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>Método CBaseControlWindow. SetWindowForeground

O `SetWindowForeground` método move a janela de vídeo para o primeiro plano e, opcionalmente, dá o foco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Foco* 
</dt> <dd>

Valor que especifica se a janela de vídeo receberá o foco. Um valor de 1 dá ao foco da janela e 0 não.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                                           | Descrição                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | O foco não é igual a 1 ou 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O filtro atual não está conectado a um grafo de filtro completo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




