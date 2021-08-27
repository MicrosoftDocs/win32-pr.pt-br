---
description: O método CheckSizes verifica as propriedades de alocador em relação ao tipo de mídia atual.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Método CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070c0cac981f73ea6fa7e3c0ecb620e262f744edd651571be9b592840ad23956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076226"
---
# <a name="cimageallocatorchecksizes-method"></a>Método CImageAllocator. CheckSizes

O `CheckSizes` método verifica as propriedades de alocador em relação ao tipo de mídia atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRequest* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que descreve as propriedades de alocador solicitadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                           | Descrição                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | As propriedades solicitadas são compatíveis com o tipo de mídia.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | As propriedades solicitadas não são compatíveis com o tipo de mídia.<br/> |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN proprietário não está conectado.<br/>                                 |



 

## <a name="remarks"></a>Comentários

Quando o método retornar, se o valor de retorno for S \_ OK, o membro **cbBuffer** da *pRequest* conterá o tamanho real do buffer. Isso pode ser maior que o tamanho solicitado, mas nunca será menor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




