---
description: O método CreateInstance cria uma instância do objeto. Esse método dá suporte à criação do objeto por meio de uma fábrica de classes. Para obter mais informações, consulte CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Método CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5060e2e9842022d89c49e01b56967a92b71c5752e01239fd970c881ccb509cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908056"
---
# <a name="cseekingpassthrucreateinstance-method"></a>Método CSeekingPassThru. CreateInstance

O `CreateInstance` método cria uma instância do objeto. Esse método dá suporte à criação do objeto por meio de uma fábrica de classes. Para obter mais informações, consulte [**CFactoryTemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Sintaxe


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para um novo objeto **CSeekingPassThru** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Seekpt. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




