---
description: Método CBaseMediaFilter. streamtime – o método streamtime recupera a hora atual do fluxo.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter. streamtime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096244"
---
# <a name="cbasemediafilterstreamtime-method"></a>Método CBaseMediaFilter. streamtime

O `StreamTime` método recupera a hora atual do fluxo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStream* \[ referência\]
</dt> <dd>

Referência a um objeto [**CRefTime**](creftime.md) que recebe a hora atual do fluxo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                      | Descrição                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Sucesso.<br/>                         |
| <dl> <dt>**VFW \_ E \_ sem \_ relógio**</dt> </dl> | Nenhum relógio de referência está disponível.<br/> |



 

## <a name="remarks"></a>Comentários

O tempo de transmissão é definido como o tempo de referência atual (conforme fornecido pelo relógio de referência) menos a hora de início (especificada por [**CBaseMediaFilter:: m \_ tStart**](cbasemediafilter-m-tstart.md)). Um carimbo de data/hora de um exemplo de mídia especifica o tempo de transmissão quando ele deve ser renderizado. Se um exemplo com um carimbo de data/hora menor que o tempo atual do fluxo ainda não tiver sido renderizado, ele será atrasado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




