---
description: Construtor de CImageSample. CImageSample-método de construtor.
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
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095604"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




