---
description: Ocorre quando um ou mais objetos IInkStrkeDisp são adicionados à coleção InkStrkes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Evento InkPicture.StrokesAdded (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5f9418289ac996b2c2248c2cf1696e7d45b4548dbafa4dff9494e76cbedc30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717399"
---
# <a name="inkpicturestrokesadded-event"></a>Evento InkPicture.StrokesAdded

Ocorre quando um ou mais [**objetos IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) são adicionados à [coleção InkStrkes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

## <a name="syntax"></a>Sintaxe


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StrokeIds* \[ Em\]
</dt> <dd>

A matriz de inteiros de identificadores para [**cada objeto IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) adicionado quando esse evento ocorre.

Para obter mais informações sobre a estrutura VARIANT, consulte [Usando a biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkStrkesEvents.** A interface **\_ IInkStrkesEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ SEStrokesAdded.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

