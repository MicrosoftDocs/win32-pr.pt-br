---
description: A função GetInterface recupera um ponteiro de interface.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Função GetInterface (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785345"
---
# <a name="getinterface-function"></a>Função GetInterface

A `GetInterface` função recupera um ponteiro de interface.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** .

</dd> <dt>

*ppv* 
</dt> <dd>

Endereço de um ponteiro para a interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro executa um incremento thread-safe da contagem de referência. Para recuperar a interface e adicionar uma referência, chame essa função de sua implementação de substituição do método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




