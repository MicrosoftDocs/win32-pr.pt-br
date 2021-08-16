---
description: O método SetProperties especifica o número de buffers a alocar e o tamanho de cada buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator.SetProperties (Amfilter.h)
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
ms.openlocfilehash: 5c5a145e630101bda4d060058cde7bfd91796386f0915e9e5329f63ced43ef19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821961"
---
# <a name="cmemallocatorsetproperties-method"></a>Método CMemAllocator.SetProperties

O `SetProperties` método especifica o número de buffers a alocar e o tamanho de cada buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Prequest* 
</dt> <dd>

Ponteiro para uma [**estrutura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.

</dd> <dt>

*Pactual* 
</dt> <dd>

Ponteiro para uma **estrutura ALLOCATOR \_ PROPERTIES** que recebe as propriedades reais do buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                 | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Êxito.<br/>                                                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                   | Argumento de ponteiro **NULL.**<br/>                                 |
| <dl> <dt>**VFW \_ E JÁ FORAM \_ \_ COMPROMETIDOS**</dt> </dl>   | Não é possível alterar a memória alocada enquanto o filtro estiver ativo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Foi especificado um alinhamento inválido.<br/>                        |
| <dl> <dt>**BUFFERS VFW \_ E \_ \_ PENDENTES**</dt> </dl> | Um ou mais buffers ainda estão ativos.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseAllocator::SetProperties.**](cbaseallocator-setproperties.md)

O alinhamento do buffer, especificado pelo **membro cbAlign** da estrutura **ALLOCATOR \_ PROPERTIES,** deve ter uma potência de dois.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




