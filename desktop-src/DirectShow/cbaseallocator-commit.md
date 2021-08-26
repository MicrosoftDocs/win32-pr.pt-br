---
description: 'O método Commit aloca a memória para os buffers. Esse método implementa o método IMemAllocator:: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Método CBaseAllocator. Commit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087576"
---
# <a name="cbaseallocatorcommit-method"></a>Método CBaseAllocator. Commit

O `Commit` método aloca a memória para os buffers. Esse método implementa o método [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da lista a seguir.



| Código de retorno                                                                                       | Descrição                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Os requisitos de buffer não foram especificados.<br/> |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) para especificar os requisitos de buffer.

Esse método chama o método virtual [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) para alocar a memória para os buffers. As classes derivadas podem substituir a **alocação**. Se uma operação de desconfirmação estiver pendente, ela será cancelada.

Você deve chamar esse método antes de chamar o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




