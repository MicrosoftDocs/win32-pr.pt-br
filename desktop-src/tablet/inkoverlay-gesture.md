---
description: Evento InkOverlay.Gesture – ocorre quando um gesto específico do aplicativo é reconhecido.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay.Gesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01689465e9951a5b8cd6548cabb0be4a0bde32c7cf46c2ea4c71b3bb38151eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219307"
---
# <a name="inkoverlaygesture-event"></a>Evento InkOverlay.Gesture

Ocorre quando um gesto específico do aplicativo é reconhecido.

## <a name="syntax"></a>Sintaxe


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cursor* \[ Em\]
</dt> <dd>

O [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o [**evento Gesture.**](inkcollector-gesture.md)

</dd> <dt>

*Traços* \[ Em\]
</dt> <dd>

A [coleção IInkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o reconhecedor retornou como o gesto.

</dd> <dt>

*Gestos* \[ Em\]
</dt> <dd>

Uma matriz de [**objetos IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) em ordem de confiança, do reconhecedor.

Para obter mais informações sobre a estrutura VARIANT, consulte [Usando a biblioteca COM](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Se a coleção desse gesto deve ser cancelada, como não apagar a tinta e disparar o [**evento Stroke.**](inkcollector-stroke.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente expedição \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ ICEGesture.

Quando a [**propriedade CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) é definida como [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), o tempo máximo entre quando um usuário adiciona um gesto e quando o evento [**Gesture**](inkcollector-gesture.md) ocorre é um valor fixo que você não pode alterar programaticamente. O reconhecimento de gestos é mais rápido **no modo InkAndGesture.**

Para impedir a coleta de tinta enquanto estiver no [**modo InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   De [**definir CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) [**como InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Exclua o traço no [**evento Stroke.**](inkcollector-stroke.md)
-   Processe o gesto no [**evento Gesture.**](inkcollector-gesture.md)

Para evitar o fluxo de tinta durante a gestação, de definir a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) como **FALSE.**

Além de ao inserir tinta, o evento [**Gesto**](inkcollector-gesture.md) é acionado quando está no modo de seleção ou apagamento. Você é responsável por acompanhar o modo de edição e deve estar ciente do modo antes de interpretar o evento.

> [!Note]  
> Para reconhecer gestos, você deve usar um objeto ou controle que possa coletar tinta.

 

Gestos de aplicativo são definidos como gestos com suporte em seu aplicativo.

Para que esse evento ocorra, o objeto ou controle deve ter interesse em um conjunto de gestos de aplicativo. Para definir os objetos ou controles de interesse em um conjunto de gestos, chame o [**método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) do objeto ou controle.

Para ver uma lista de gestos específicos do aplicativo, consulte o tipo de enumeração [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

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

[**Enumeração InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> </dl>

 

