---
description: 'Ocorre quando o controle InkEdit Obtém os resultados manualmente de uma chamada para o método InkEdit:: Recognize ou automaticamente após o tempo limite do reconhecimento ser acionado.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit. RecognitionResult (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef71d38be31f32c59919a9ce4f24fd90b2d188d86a26e81821f6f7987da31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939076"
---
# <a name="inkeditrecognitionresult-event"></a>Evento InkEdit. RecognitionResult

Ocorre quando o controle [InkEdit](inkedit-control-reference.md) Obtém os resultados manualmente de uma chamada para o método [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automaticamente após o tempo limite do reconhecimento ser acionado.

## <a name="syntax"></a>Sintaxe


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RecognitionResult* \[ no\]
</dt> <dd>

Um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) que contém o resultado do reconhecimento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeRecognitionResult DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Reconhecer o \[ controle de método InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

