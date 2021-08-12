---
description: Método CMediaEvent.Invoke – fornece acesso a propriedades e métodos expostos por um objeto .
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Método CMediaEvent.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37fadefe3163ed4211b8112ec17cc1cfb3fb3625b4aba207db06a25de3e27b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655220"
---
# <a name="cmediaeventinvoke-method"></a>Método CMediaEvent.Invoke

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

Identificador do membro. Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) ou a documentação do objeto para obter o identificador de expedição.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Deve ser IID \_ NULL.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de localidade no qual interpretar argumentos.

</dd> <dt>

*Wflags* 
</dt> <dd>

Sinalizadores que descrevem o contexto da `CMediaEvent::Invoke` chamada.

</dd> <dt>

*Pdispparams* 
</dt> <dd>

Ponteiro para uma estrutura que contém uma matriz de argumentos, uma matriz de IDs de expedição de argumento para argumentos nomeados e conta para o número de elementos nas matrizes.

</dd> <dt>

*Pvarresult* 
</dt> <dd>

Ponteiro para onde o resultado deve ser armazenado ou **NULL** se o chamador não espera nenhum resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Ponteiro para uma estrutura que contém informações de exceção.

</dd> <dt>

*Puargerr* 
</dt> <dd>

Ponteiro para o índice do primeiro argumento, dentro da matriz **rgvarg** da estrutura **DISPPARAMS,** que tem um erro. Para obter mais informações sobre **DISPPARAMS,** consulte o SDK da plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará DISP \_ E \_ UNKNOWNINTERFACE se *riid* não for IID \_ NULL. Retorna um dos códigos de erro de [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) se a chamada falhar. Caso contrário, retornará **o HRESULT** da chamada para **IDispatch::Invoke.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




