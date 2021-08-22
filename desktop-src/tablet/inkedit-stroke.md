---
description: Ocorre quando o usuário desenha um novo objeto IInkTrikeDisp em qualquer objeto IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Evento InkEdit.Stroke (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1114f26fa17690b1651321ef15ad11d8ec4d55f11f8e7e1754d6d694fdceda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717891"
---
# <a name="inkeditstroke-event"></a>Evento InkEdit.Stroke

Ocorre quando o usuário desenha um novo objeto [**IInkTrikeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em qualquer [**objeto IInkTablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Traço* \[ Em\]
</dt> <dd>

O objeto [**IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar a coleção do [**objeto IInkStrkeDisp;**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) **VARIANT \_ FALSE** para coletar o **objeto IInkStrkeDisp** e continuar com o **Traço** mesmo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents.** A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ IeeStrke.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked.h (também requer \_ i.c com tinta)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkRogkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

