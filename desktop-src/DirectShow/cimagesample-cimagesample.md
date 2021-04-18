---
description: Método de construtor.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Construtor CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780870"
---
# <a name="cimagesamplecimagesample-constructor"></a>Construtor CImageSample. CImageSample

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para o alocador que criou este exemplo.

</dd> <dt>

*pName* 
</dt> <dd>

Ignorado.

</dd> <dt>

*phr* 
</dt> <dd>

Ignorado.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *.* O buffer deve conter um bitmap independente de dispositivo (DIB) GDI.

</dd> <dt>

*length* 
</dt> <dd>

Comprimento do buffer.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe [**CImageAllocator**](cimageallocator.md) cria um DIB usando um objeto de mapeamento de arquivo que é apoiado pelo arquivo de paginação do sistema operacional. O identificador para o objeto de mapeamento de arquivo é armazenado no membro **hMapping** da estrutura **m \_ DibData** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




