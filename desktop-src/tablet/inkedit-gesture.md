---
description: Ocorre quando um gesto de aplicativo é reconhecido.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. Gesture (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170082"
---
# <a name="inkeditgesture-event"></a>Evento InkEdit. Gesture

Ocorre quando um gesto de aplicativo é reconhecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que foi usado para criar esse gesto.

</dd> <dt>

*Traços* \[ no\]
</dt> <dd>

A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contém os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que compõem esse gesto.

</dd> <dt>

*Gestos* \[ no\]
</dt> <dd>

Uma matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , em ordem de confiança.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

Se a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que compõe esse gesto deve ser cancelada, para não apagar a tinta e disparar o evento [**Stroke**](inkedit-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de \_ IeeGesture DISPID.

Um evento de **gesto** será gerado somente se o [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) para o objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) for o primeiro objeto **IInkStrokeDisp** desde a última chamada para o método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou o último disparo do tempo limite de reconhecimento.

Se o evento de **gesto** for cancelado, o evento [**Stroke**](inkedit-stroke.md) será gerado para a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que gerou o evento de **gesto** .

Para que esse evento ocorra, o controle [InkEdit](inkedit-control-reference.md) deve assinar um conjunto de gestos de aplicativo. Para definir o interesse do controle InkEdit em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .

Para obter uma lista de gestos de aplicativo, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

O controle [InkEdit](inkedit-control-reference.md) não reconhece vários gestos de traço.

O controle [InkEdit](inkedit-control-reference.md) assina os seguintes gestos.



| Gesto                              | Ação               |
|--------------------------------------|----------------------|
| Para baixo à esquerda, para baixo-esquerda-longa<br/> | Digite<br/>     |
| Direita<br/>                     | Space<br/>     |
| Esquerda<br/>                      | Backspace<br/> |
| Para cima à direita, para cima à direita<br/>   | Tab<br/>       |



 

Para alterar a ação padrão para um gesto:

1.  Adicione manipuladores de eventos para os eventos de **gesto** e [**traço**](inkedit-stroke.md) .
2.  No manipulador de eventos de **gesto** , cancele o evento de **gesto** para o gesto e execute a ação alternativa para o gesto.
3.  No manipulador de eventos [**Stroke**](inkedit-stroke.md) , cancele o evento **Stroke** para o objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que gerou o evento de **gesto** cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Enumeração InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Controle InkEdit do método SetGestureStatus \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Propriedade RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Controle de evento InkEdit de Stroke \[\]**](inkedit-stroke.md)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> </dl>

 

