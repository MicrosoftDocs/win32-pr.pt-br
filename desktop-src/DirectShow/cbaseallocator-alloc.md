---
description: Método CBaseAllocator. Alloc – o método Alloc aloca memória para os buffers.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Método CBaseAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096356"
---
# <a name="cbaseallocatoralloc-method"></a>Método CBaseAllocator. Alloc

O `Alloc` método aloca memória para os buffers.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                       | Descrição                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>           | Os requisitos de buffer não foram alterados.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>              | Os requisitos de buffer foram alterados.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Os requisitos de buffer não foram definidos.<br/>     |



 

## <a name="remarks"></a>Comentários

Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) .

Na classe base, esse método não aloca nenhuma memória. Ele retornará um erro se os requisitos de buffer não tiverem sido definidos, S \_ false se os requisitos não foram alterados e s \_ OK se os requisitos foram alterados.

Uma classe derivada deve substituir esse método para executar a alocação de memória real. Normalmente, a classe derivada executará as seguintes etapas:

1.  Chame a implementação da classe base para determinar se a memória realmente precisa ser alocada.
2.  Aloque memória.
3.  Crie objetos [**CMediaSample**](cmediasample.md) que contenham partes de memória da etapa 2.
4.  Adicione cada objeto **CMediaSample** à lista de amostras gratuitas ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).

Para obter um exemplo, consulte [**CMemAllocator:: Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




