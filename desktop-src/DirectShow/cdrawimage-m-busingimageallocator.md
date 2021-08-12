---
description: A \_ variável de membro m bUsingImageAllocator indica se o alocador para a conexão de PIN é um objeto CImageAllocator. Se o valor for TRUE, o alocador será um objeto CImageAllocator (ou derivado dessa classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657098"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Membro de CDrawImage:: m \_ bUsingImageAllocator

A `m_bUsingImageAllocator` variável de membro indica se o alocador para a conexão de PIN é um objeto **CImageAllocator** . Se o valor for **true**, o alocador será um objeto **CImageAllocator** (ou derivado dessa classe).

## <a name="syntax"></a>Sintaxe


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Comentários

Quando o valor for **true**, o objeto **CDrawImage** poderá usar as funções **BitBlt** e **StretchBlt** do GDI para renderizar a imagem, em vez das funções de **SetDIBitsToDevice** e **StretchDIBits** mais lentas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




