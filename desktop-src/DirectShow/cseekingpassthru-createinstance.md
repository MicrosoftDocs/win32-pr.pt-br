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
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751486"
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

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para um novo objeto **CSeekingPassThru** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Seekpt. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




