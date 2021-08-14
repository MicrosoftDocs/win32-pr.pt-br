---
description: Ocorre quando o usuário libera uma chave enquanto o controle InkEdit tem foco.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Evento InkEdit.KeyUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ac908202a22fc1f564c3f21da4cc3cce2e79e2f093ec93b65ff56066f94510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220751"
---
# <a name="inkeditkeyup-event"></a>Evento InkEdit.KeyUp

Ocorre quando o usuário libera uma chave enquanto o [controle InkEdit](inkedit-control-reference.md) tem foco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pkey* 
</dt> <dd>

O código de chave virtual da chave pressionada pelo usuário.

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Um membro da [**enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais chaves modificadores são desfeitas no momento do evento.



| Valor                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Deslocamento de \_ IKM**</dt> </dl>             | Especifica que a tecla SHIFT foi usada como um modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Controle**</dt> </dl> | Especifica que a tecla CTRL foi usada como um modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que a tecla ALT foi usada como um modificador. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents.** A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ IeeKeyUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Inked.h (também requer \_ i.c com tinta)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeração InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Controle InkEdit do evento KeyDown \[\]**](inkedit-keydown.md)
</dt> <dt>

[**Controle InkEdit do evento KeyPress \[\]**](inkedit-keypress.md)
</dt> </dl>

 

