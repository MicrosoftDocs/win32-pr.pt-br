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
ms.openlocfilehash: 87a6768c8864de45d50dc630773b756dfad43759adbf4b09ed8070febd37f4d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635466"
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

*Foca* 
</dt> <dd>

Valor que especifica se a janela de vídeo receberá o foco. Um valor de 1 dá ao foco da janela e 0 não.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                                           | Descrição                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | O foco não é igual a 1 ou 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O filtro atual não está conectado a um grafo de filtro completo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




