---
description: A função GetInterface recupera um ponteiro de interface.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Função GetInterface (Combase.h)
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
ms.openlocfilehash: 289c6e56d4b5387fe9224e476c69865107102141b687825cdfd9a717f482632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537026"
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

*Punk* 
</dt> <dd>

Ponteiro para a interface **IUnknown.**

</dd> <dt>

*Ppv* 
</dt> <dd>

Endereço de um ponteiro para a interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro executa um incremento thread-safe da contagem de referência. Para recuperar a interface e adicionar uma referência, chame essa função de sua implementação de substituição do **método INonDeltingUnknown::NonDeltingQueryInterface.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> <dt>

[**Inondelegatingunknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




