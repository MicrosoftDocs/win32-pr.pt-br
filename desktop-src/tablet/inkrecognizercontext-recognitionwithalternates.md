---
description: Ocorre quando a classe InkRecognizerContext gerou resultados depois de chamar o método de método BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170467"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Evento InkRecognizerContext. RecognitionWithAlternates

Ocorre quando a [**classe InkRecognizerContext**](inkrecognizercontext-class.md) gerou resultados depois de chamar o método de [**método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .

## <a name="syntax"></a>Sintaxe


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RecognitionResult* \[ no\]
</dt> <dd>

O resultado de reconhecimento do evento.

</dd> <dt>

*CustomData* \[ no\]
</dt> <dd>

Os dados personalizados para o resultado do reconhecimento.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ no\]
</dt> <dd>

O status de reconhecimento a partir do resultado de reconhecimento mais recente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O comportamento da API (interface de programação de aplicativo) é imprevisível se você tentar obter acesso ao objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original do manipulador de eventos de reconhecimento. Não tente fazer isso. Em vez disso, se você precisar fazer isso, crie um sinalizador e defina-o no manipulador de eventos de [**reconhecimento**](inkrecognizercontext-recognition.md) . Em seguida, você pode sondar esse sinalizador para determinar quando alterar as propriedades **InkRecognizerContext** fora do manipulador de eventos.

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IRERecognitionWithAlternates DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[**Método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Método Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

