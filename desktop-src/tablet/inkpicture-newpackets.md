---
description: Evento InkPicture. NewPackets – ocorre quando o coletor de tinta recebe um pacote.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11568d898bb6f152b5d430cf1f347390174c16a51b0572e45ddd3528c8e0dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451084"
---
# <a name="inkpicturenewpackets-event"></a>Evento InkPicture. NewPackets

Ocorre quando o coletor de tinta recebe um pacote.

## <a name="syntax"></a>Sintaxe


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**NewInAirPackets**](inkpicture-newinairpackets.md) .

</dd> <dt>

*Traço* \[ no\]
</dt> <dd>

O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketCount* \[ no\]
</dt> <dd>

O número de pacotes recebidos para um objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*PacketData* \[ entrada, saída\]
</dt> <dd>

Uma matriz que contém os dados selecionados para o pacote.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Os pacotes são recebidos enquanto um traço está sendo coletado. Os eventos de pacote ocorrem rapidamente e um manipulador de eventos **NewPackets** deve ser rápido ou o desempenho sofre.

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICENewPackets de DISPID \_ .

Esse evento deve ser usado com cuidado, pois ele pode ter um efeito adverso no desempenho da tinta se um código excessivo for executado nos manipuladores de eventos.

Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta. A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.

> [!Note]  
> Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento NewInAirPackets**](inkpicture-newinairpackets.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




