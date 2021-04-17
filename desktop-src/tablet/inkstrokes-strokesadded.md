---
description: Ocorre quando um ou mais traços são adicionados à coleção InkStrokes.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Evento InkStrokes. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811730"
---
# <a name="inkstrokesstrokesadded-event"></a>Evento InkStrokes. StrokesAdded

Ocorre quando um ou mais traços são adicionados à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

## <a name="syntax"></a>Sintaxe


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StrokeIds* \[ no\]
</dt> <dd>

A matriz de inteiros de identificadores para cada objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) adicionado quando esse evento ocorre.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ SEStrokesAdded DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Adicionar coleção de métodos \[ InkStrokes\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> </dl>

 

