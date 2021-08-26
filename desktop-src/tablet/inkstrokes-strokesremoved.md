---
description: Ocorre quando um ou mais traços são excluídos da coleção InkStrkes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Evento InkStrkes.StrokesRemoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a5c4f7d53f88c50efd77e537cfa311f08ab168abdb4a05392286fb6c0b6b4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934856"
---
# <a name="inkstrokesstrokesremoved-event"></a>Evento InkStrkes.StrokesRemoved

Ocorre quando um ou mais traços são excluídos da [coleção InkStrkes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

## <a name="syntax"></a>Sintaxe


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StrokeIds* \[ Em\]
</dt> <dd>

A matriz de inteiros de identificadores para [**cada objeto IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) excluído quando esse evento ocorre.

Para obter mais informações sobre a estrutura VARIANT, consulte [Usando a biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador DISPID \_ SEStrokesRemoved.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleção InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Remover coleção \[ InkStrkes do método\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> </dl>

 

