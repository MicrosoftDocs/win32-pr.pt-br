---
description: 'O método de alocação aloca memória para os buffers. Esse método substitui o método CBaseAllocator:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Método CImageAllocator. Alloc (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bdf4c36bcf66d46a5c5ee7df16ac04a4461bd3a88de91e175b81e89ce496e1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076236"
---
# <a name="cimageallocatoralloc-method"></a>Método CImageAllocator. Alloc

O `Alloc` método aloca memória para os buffers. Esse método substitui o método [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                   | Descrição                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) , quando o filtro confirma o alocador.

Esse método cria uma lista de amostras de mídia, que são implementadas como objetos [**CImageSample**](cimagesample.md) . Cada exemplo contém um bitmap independente de dispositivo GDI, usando a função **CreateDIBSection** do GDI.

Internamente, esse método chama [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) para criar cada DIB e [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) para criar cada exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




