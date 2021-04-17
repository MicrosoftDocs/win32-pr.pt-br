---
description: 'O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método implementa o método IMemAllocator:: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Método CBaseAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812995"
---
# <a name="cbaseallocatorsetproperties-method"></a>Método CBaseAllocator. SetProperties

O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método implementa o método [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .

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

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                                 | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Êxito.<br/>                                                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                   | Argumento de ponteiro **nulo** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ já \_ confirmado**</dt> </dl>   | Não é possível alterar a memória alocada enquanto o filtro estiver ativo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Foi especificado um alinhamento inválido.<br/>                        |
| <dl> <dt>**VFW \_ E \_ buffers \_ pendentes**</dt> </dl> | Um ou mais buffers ainda estão ativos.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esse método especifica os requisitos de buffer, mas não aloca nenhum buffer. Chame o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) para alocar buffers.

O chamador aloca duas estruturas de propriedades de ALOCAdor \_ . O parâmetro de *pRequest* contém os requisitos de buffer do chamador, incluindo o número de buffers e o tamanho de cada buffer. Quando o método retorna, o parâmetro *Pactual* contém as propriedades de buffer reais, conforme definido pelo alocador. Na classe base, supondo que o método tenha sucesso, as propriedades reais sempre correspondem às propriedades solicitadas. Classes derivadas podem substituir esse comportamento.

O alocador não deve ser confirmado e não deve ter buffers pendentes. Na classe base, o alinhamento deve ser igual a 1. A classe [**CMemAllocator**](cmemallocator.md) substitui esse requisito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




