---
description: O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778497"
---
# <a name="cmemallocatorsetproperties-method"></a>Método CMemAllocator. SetProperties

O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRequest* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Ponteiro para uma estrutura de **\_ Propriedades de alocador** que recebe as propriedades reais do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                 | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Êxito.<br/>                                                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                   | Argumento de ponteiro **nulo** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ já \_ confirmado**</dt> </dl>   | Não é possível alterar a memória alocada enquanto o filtro estiver ativo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Foi especificado um alinhamento inválido.<br/>                        |
| <dl> <dt>**VFW \_ E \_ buffers \_ pendentes**</dt> </dl> | Um ou mais buffers ainda estão ativos.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .

O alinhamento do buffer, especificado pelo membro **cbAlign** da estrutura **de \_ Propriedades do alocador** , deve ser uma potência par de dois.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




