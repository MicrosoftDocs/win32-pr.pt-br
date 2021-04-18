---
description: 'Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados nas chamadas subsequentes para a função de membro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757318"
---
# <a name="cmediaeventgetidsofnames-method"></a>Método CMediaEvent. GetIDsOfNames

Mapeia uma única função de membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados nas chamadas subsequentes para a função de membro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de referência. Reservado para uso futuro. Deve ser **NULL**.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Endereço de um ponteiro para uma matriz de nomes passada para ser mapeada.

</dd> <dt>

*cNames* 
</dt> <dd>

Contagem dos nomes a serem mapeados.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de localidade no qual interpretar os nomes.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Ponteiro para uma matriz alocada pelo chamador, cada elemento que contém uma ID correspondente a um dos nomes passados na matriz *rgszNames* . O primeiro elemento representa o nome do membro; os elementos subsequentes representam cada um dos parâmetros do membro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_E/ \_ ou \_ CLSID desconhecido**</dt> </dl> | O CLSID não foi reconhecido.<br/>                                                                                                             |
| <dl> <dt>**Não receber \_ E não \_ conhecido**</dt> </dl>    | Um ou mais dos nomes não eram conhecidos. Os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Sem memória.<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




