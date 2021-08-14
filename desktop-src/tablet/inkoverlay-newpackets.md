---
description: Ocorre quando a tinta coleta um pacote.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Evento InkOverlay.NewPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2571e7c8f97881da5bbbef6cdab093ce2d3107b5482def5b62d2dfa141c7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219192"
---
# <a name="inkoverlaynewpackets-event"></a>Evento InkOverlay.NewPackets

Ocorre quando o ink collecto rerreceives a um pacote

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

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o [**evento NewInAirPackets.**](inkcollector-newinairpackets.md)

</dd> <dt>

*Traço* \[ Em\]
</dt> <dd>

Especifica o [**objeto IInkStrkeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketCount* \[ Em\]
</dt> <dd>

O número de pacotes recebidos para um [**objeto IInkStrkeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Uma matriz que contém os dados selecionados para o pacote.

Para obter mais informações sobre a estrutura VARIANT, consulte [Usando a biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Os pacotes são recebidos enquanto um traço está sendo coletado. Eventos de pacote ocorrem rapidamente e um manipulador de eventos [**NewPackets**](inkcollector-newpackets.md) deve ser rápido ou o desempenho é prejudicado.

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICENewPackets.

Esse evento deve ser usado com cuidado, pois poderá ter um efeito adverso no desempenho da tinta se um código demais for executado nos manipuladores de eventos.

Para definir quais propriedades estão contidas nessa matriz, use a [**propriedade DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta. A matriz retornada *pelo parâmetro PacketData* contém os dados dessas propriedades.

> [!Note]  
> Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Evento NewInAirPackets**](inkcollector-newinairpackets.md)
</dt> <dt>

[**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkRogkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




