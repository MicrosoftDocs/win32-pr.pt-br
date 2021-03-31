---
description: Ocorre quando um pacote no ar é visto.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171166"
---
# <a name="inkoverlaynewinairpackets-event"></a>Evento InkOverlay. NewInAirPackets

Ocorre quando um pacote no ar é visto.

## <a name="syntax"></a>Sintaxe


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .

</dd> <dt>

*PacketCount* \[ no\]
</dt> <dd>

O número de pacotes no ar recebidos.

</dd> <dt>

*PacketData* \[ entrada, saída\]
</dt> <dd>

Uma matriz que contém os dados selecionados para o pacote.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Um pacote no ar é criado quando um usuário move uma caneta perto do Tablet e o cursor está dentro da janela do objeto do coletor de tinta ou o usuário move um mouse dentro da janela associada do objeto do coletor de tinta. Os eventos [**NewInAirPackets**](inkcollector-newinairpackets.md) são gerados rapidamente, e o manipulador de eventos deve ser rápido ou o desempenho sofre.

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICENewInAirPackets de DISPID \_ .

O evento [**NewInAirPackets**](inkcollector-newinairpackets.md) é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta. Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.

Para definir quais propriedades estão contidas nessa matriz, use a propriedade [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) do objeto do coletor de tinta. A matriz que o parâmetro *PacketData* retorna contém os dados para essas propriedades.

> [!Note]  
> Embora você possa modificar os dados do pacote, essas modificações não são persistentes ou usadas.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**Propriedade DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**Evento NewPackets**](inkcollector-newpackets.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




