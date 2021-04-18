---
description: O método de alocação aloca memória para os buffers.
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
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756652"
---
# <a name="cbaseallocatoralloc-method"></a>Método CBaseAllocator. Alloc

O `Alloc` método aloca memória para os buffers.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




