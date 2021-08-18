---
description: Ocorre quando InkRecognizerContext gerou resultados do método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext.Recognition (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f6c4799f3366003d14451a19a7bea19ea35aadcce9226f25f1fe80a14ab19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966935"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext.Recognition

Ocorre quando [**InkRecognizerContext**](inkrecognizercontext-class.md) gerou resultados do [**método BackgroundRecognize.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)

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

*RecognizedString* \[ Em\]
</dt> <dd>

O texto do resultado do reconhecimento com a maior confiança.

Para obter mais informações sobre o tipo de dados BSTR, consulte [Usando a biblioteca COM.](using-the-com-library.md)

</dd> <dt>

*CustomData* \[ Em\]
</dt> <dd>

O objeto que contém os dados personalizados para o resultado do reconhecimento.

Para obter mais informações sobre a estrutura VARIANT, consulte [Usando a biblioteca COM.](using-the-com-library.md)

</dd> <dt>

*RecognitionStatus* \[ Em\]
</dt> <dd>

O status de reconhecimento a partir do resultado de reconhecimento mais recente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O comportamento da API (interface de programação de aplicativo) será imprevisível se você tentar obter acesso ao objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original do manipulador de eventos de reconhecimento. Não tente fazer isso. Em vez disso, se você precisar fazer isso, crie um sinalizador e de definido no manipulador [de](ink-recognition.md) eventos reconhecimento. Em seguida, você pode sondar esse sinalizador para determinar quando alterar as **propriedades InkRecognizerContext** fora do manipulador de eventos.

Esse método de evento é definido na \_ interface IInkEvents. A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ DISPID IRERecognition.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
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

[**IInkRecognitionResult Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

