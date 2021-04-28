---
description: Método CMediaPosition. GetIDsOfNames – o método GetIDsOfNames mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095524"
---
# <a name="cmediapositiongetidsofnames-method"></a>Método CMediaPosition. GetIDsOfNames

O `GetIDsOfNames` método mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.

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

Reservado. Use o IID \_ nulo.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Endereço de uma matriz de cadeias de caracteres largos que contêm os nomes a serem mapeados.

</dd> <dt>

*cNames* 
</dt> <dd>

Tamanho da matriz fornecida pelo parâmetro *rgszNames* .

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de localidade no qual interpretar os nomes. Pode ser **NULL**.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Ponteiro para uma matriz que recebe os DISPIDs. Cada elemento de recebe um identificador que corresponde a um dos nomes passados no parâmetro *rgszNames* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                         | Descrição                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Sucesso.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memória insuficiente.<br/>                     |
| <dl> <dt>**Não receber \_ E não \_ conhecido**</dt> </dl> | Um ou mais dos nomes não eram conhecidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




