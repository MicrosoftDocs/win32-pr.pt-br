---
description: Ocorre quando o InkRecognizerContext gerou resultados do método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762200"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext. Recognition

Ocorre quando o [**InkRecognizerContext**](inkrecognizercontext-class.md) gerou resultados do método [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .

## <a name="syntax"></a>Sintaxe


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Reconhecívelstring* \[ no\]
</dt> <dd>

O texto de resultado do reconhecimento com a maior confiança.

Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ no\]
</dt> <dd>

O objeto que contém os dados personalizados para o resultado do reconhecimento.

Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ no\]
</dt> <dd>

O status de reconhecimento a partir do resultado de reconhecimento mais recente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O comportamento da API (interface de programação de aplicativo) é imprevisível se você tentar obter acesso ao objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original do manipulador de eventos de reconhecimento. Não tente fazer isso. Em vez disso, se você precisar fazer isso, crie um sinalizador e defina-o no manipulador de eventos de [reconhecimento](ink-recognition.md) . Em seguida, você pode sondar esse sinalizador para determinar quando alterar as propriedades **InkRecognizerContext** fora do manipulador de eventos.

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IRERecognition DISPID.

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

[**Método BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Enumeração InkRecognitionStatus**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Método Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

