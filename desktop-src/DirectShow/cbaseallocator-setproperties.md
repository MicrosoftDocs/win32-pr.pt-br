---
description: O método SetProperties especifica o número de buffers a alocar e o tamanho de cada buffer. Esse método implementa o método IMemAllocator::SetProperties.
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Método CBaseAllocator.SetProperties (Amfilter.h)
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
ms.openlocfilehash: d81ee1c29f1c9e2cc9927f926144a7427b5e94f72406f94ce65f7d4a20e2ab32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057476"
---
# <a name="cbaseallocatorsetproperties-method"></a>Método CBaseAllocator.SetProperties

O `SetProperties` método especifica o número de buffers a alocar e o tamanho de cada buffer. Esse método implementa o [**método IMemAllocator::SetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)

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

Retorna um dos seguintes **valores HRESULT.**



| Código de retorno                                                                                                 | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Êxito.<br/>                                                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                   | Argumento de ponteiro **NULL.**<br/>                                 |
| <dl> <dt>**VFW \_ E JÁ FORAM \_ \_ COMPROMETIDOS**</dt> </dl>   | Não é possível alterar a memória alocada enquanto o filtro estiver ativo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Foi especificado um alinhamento inválido.<br/>                        |
| <dl> <dt>**BUFFERS VFW \_ E \_ \_ PENDENTES**</dt> </dl> | Um ou mais buffers ainda estão ativos.<br/>                      |



 

## <a name="remarks"></a>Comentários

Esse método especifica os requisitos de buffer, mas não aloca nenhum buffer. Chame o [**método CBaseAllocator::Commit**](cbaseallocator-commit.md) para alocar buffers.

O chamador aloca duas estruturas ALLOCATOR \_ PROPERTIES. O *parâmetro pRequest* contém os requisitos de buffer do chamador, incluindo o número de buffers e o tamanho de cada buffer. Quando o método retorna, o *parâmetro pActual* contém as propriedades reais do buffer, conforme definido pelo alocador. Na classe base, supondo que o método seja bem-sucedido, as propriedades reais sempre corresponderão às propriedades solicitadas. Classes derivadas podem substituir esse comportamento.

O alocador não deve ser confirmado e não deve ter buffers pendentes. Na classe base, o alinhamento deve ser igual a 1. A [**classe CMemAllocator**](cmemallocator.md) substitui esse requisito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




