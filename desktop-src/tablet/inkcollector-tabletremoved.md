---
description: Evento InkCollector.TabletRemoved – ocorre quando um IInkTablet é removido do sistema.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Evento InkCollector.TabletRemoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d3c319a4e67a22c81a74c6b5acceba7bd6f19188042fc68ebe4c7c7c8314e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773516"
---
# <a name="inkcollectortabletremoved-event"></a>Evento InkCollector.TabletRemoved

Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.

## <a name="syntax"></a>Sintaxe


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TabletId* \[ Em\]
</dt> <dd>

O valor longo que foi usado como a ID do [**objeto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents \_ e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICETabletRemoved.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**IInkTablet Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




