---
description: Evento InkPicture. CursorInRange – ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: Evento InkPicture. CursorInRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a44b41e9eaffa4cb7a6939e1e6b8caf55cb7fbb8782d75cda490e4dc3d34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042097"
---
# <a name="inkpicturecursorinrange-event"></a>Evento InkPicture. CursorInRange

Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorInRange** .

</dd> <dt>

*NewCursor* \[ no\]
</dt> <dd>

**Variante \_ TRUE** se esta for a primeira vez que esse coletor de tinta entrou em contato com o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorInRange** ; caso contrário, **Variant \_ false**.

</dd> <dt>

*Botõesstate* \[ no\]
</dt> <dd>

O estado dos botões para o cursor que gerou o evento **CursorInRange** .

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido em **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interface somente de expedição) com uma ID de \_ ICECursorInRange DISPID.

O evento **CursorInRange** é disparado mesmo quando estiver no modo de seleção ou apagamento, não apenas quando estiver no modo de tinta. Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento. A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.

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

[**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)
</dt> <dt>

[**Enumeração InkCursorButtonState**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




