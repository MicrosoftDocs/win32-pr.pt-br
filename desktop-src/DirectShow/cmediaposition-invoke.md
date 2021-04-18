---
description: O método Invoke fornece acesso a propriedades e métodos expostos pelo objeto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Método CMediaPosition. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769229"
---
# <a name="cmediapositioninvoke-method"></a>Método CMediaPosition. Invoke

O `Invoke` método fornece acesso a propriedades e métodos expostos pelo objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dispidMember* 
</dt> <dd>

Identificador do membro. Use [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) para obter o identificador de expedição.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Deve ser um IID \_ nulo.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de localidade no qual interpretar argumentos.

</dd> <dt>

*wFlags* 
</dt> <dd>

Sinalizadores que descrevem o contexto da chamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Ponteiro para uma estrutura **DIPPARAMS** que contém os argumentos.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Ponteiro para uma **variante** que recebe o resultado, ou **NULL** se o chamador não espera nenhum resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Ponteiro para uma estrutura que recebe informações de exceção.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Aponta para uma variável que recebe o índice do primeiro argumento que causa um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                              | Descrição                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Êxito.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | O parâmetro *riid* não é nulo de IID \_<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




