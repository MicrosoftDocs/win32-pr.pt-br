---
description: Método CMediaControl. Invoke – fornece acesso a propriedades e métodos expostos por um objeto.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Método CMediaControl. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085634"
---
# <a name="cmediacontrolinvoke-method"></a>Método CMediaControl. Invoke

Fornece acesso a propriedades e métodos expostos por um objeto.

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

Identificador do membro. Use [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md) ou a documentação do objeto para obter o identificador de expedição.

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

Sinalizadores que descrevem o contexto da `CMediaControl::Invoke` chamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Ponteiro para uma estrutura que contém uma matriz de argumentos, uma matriz de IDs de expedição de argumento para argumentos nomeados e contagens para o número de elementos nas matrizes.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Ponteiro para onde o resultado deve ser armazenado, ou **NULL** se o chamador não espera nenhum resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Ponteiro para uma estrutura que contém informações de exceção.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Ponteiro para o índice do primeiro argumento, dentro da matriz **rgvarg** da estrutura **DISPPARAMS** , que tem um erro. Para obter mais informações sobre o **DISPPARAMS**, consulte o SDK da plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o DISP \_ E \_ UNKNOWNINTERFACE se *riid* não for \_ nulo como IID. Retorna um dos códigos de erro de [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) se a chamada falhar. Caso contrário, retorna o **HRESULT** da chamada para **IDispatch:: Invoke**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




