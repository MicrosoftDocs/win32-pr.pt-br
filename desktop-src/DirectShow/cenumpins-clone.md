---
description: O método Clone faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o método IEnumPins::Clone.
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Método CEnumPins.Clone (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a0d14f0caf30f6037d53639ff54d2e21d6d0fb0eee5cfa493aba248e84d48e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688606"
---
# <a name="cenumpinsclone-method"></a>Método CEnumPins.Clone

O `Clone` método faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o [**método IEnumPins::Clone.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ppenum* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) do novo enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Memória insuficiente.<br/>                                                        |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                  | Argumento de ponteiro **NULL.**<br/>                                                  |
| <dl> <dt>**VFW \_ \_ ENUM \_ FORA DE \_ \_ SINCRONIA**</dt> </dl> | O estado do filtro foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




