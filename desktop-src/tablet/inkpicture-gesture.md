---
description: Evento InkPicture. Gesture-ocorre quando um gesto específico do aplicativo é reconhecido.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c0307397fc5a197666894d40adce6f4a579e22d896df8df645b053580ee94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451056"
---
# <a name="inkpicturegesture-event"></a>Evento InkPicture. Gesture

Ocorre quando um *gesto* específico do aplicativo é reconhecido.

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

*Cursor* \[ no\]
</dt> <dd>

O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento de **gesto** .

</dd> <dt>

*Traços* \[ no\]
</dt> <dd>

A coleção [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o reconhecedor retornou como gesto.

</dd> <dt>

*Gestos* \[ no\]
</dt> <dd>

Uma matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , em ordem de confiança, do reconhecedor.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

**Variante \_ TRUE** se esse evento deve ser cancelado, como não apagar a tinta e disparar o evento [**Stroke**](inkpicture-stroke.md) . Caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICEGesture de DISPID \_ .

Quando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) é definida como [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), o tempo limite entre quando um usuário adiciona um gesto e quando o evento de **gesto** ocorre é um valor fixo que você não pode alterar programaticamente. O reconhecimento de gestos é mais rápido no modo **InkAndGesture** .

Para evitar a coleta de tinta no modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Defina [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) como [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Exclua o traço no evento de [**traço**](inkpicture-stroke.md) .
-   Processe o gesto no evento de **gesto** .

Para evitar o fluxo de tinta enquanto gesturing, defina a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) como **false**.

Além de ao inserir tinta, o evento de **gesto** é acionado no modo de seleção ou apagamento. Você é responsável por controlar o modo de edição e deve estar ciente do modo antes de interpretar o evento.

> [!Note]  
> Para reconhecer gestos, você deve usar um objeto ou controle que possa coletar tinta.

 

Os gestos de aplicativo são definidos como gestos com suporte no seu aplicativo.

Para que esse evento ocorra, o objeto ou controle deve ter interesse em um conjunto de gestos de aplicativo. Para definir os objetos ou controles de interesse em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) do objeto ou controle.

Para obter uma lista de gestos de aplicativo específicos, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Enumeração InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> </dl>

 

