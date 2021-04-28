---
description: Evento InkCollector. Gesture-ocorre quando um gesto específico do aplicativo é reconhecido.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Evento InkCollector. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110184"
---
# <a name="inkcollectorgesture-event"></a>Evento InkCollector. Gesture

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

**Variante \_ TRUE** se este gesto deve ser cancelado; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICEGesture de DISPID \_ .

Quando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) é definida como [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), o tempo limite entre quando um usuário adiciona um gesto e quando o evento de **gesto** ocorre é um valor fixo que você não pode alterar programaticamente. O reconhecimento de gestos é mais rápido no modo **InkAndGesture** .

Para evitar a coleta de tinta no modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Defina [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) como [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Exclua o traço no evento de [**traço**](inkcollector-stroke.md) .
-   Processe o gesto no evento de **gesto** .

Para evitar o fluxo de tinta enquanto gesturing, defina a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) como **false**.

Além de ao inserir tinta, o evento de **gesto** é acionado no modo de seleção ou apagamento. Você é responsável por controlar o modo de edição e deve estar ciente do modo antes de interpretar o evento.

> [!Note]  
> Para reconhecer gestos, você deve usar um objeto ou controle que possa coletar tinta.

 

Os gestos de aplicativo são definidos como gestos com suporte no seu aplicativo.

Para que esse evento ocorra, o objeto ou controle deve ter interesse em um conjunto de gestos de aplicativo. Para definir os objetos ou controles de interesse em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) do objeto ou controle.

Para obter uma lista de gestos de aplicativo específicos, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Enumeração InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Usando gestos](using-gestures.md)
</dt> </dl>

 

