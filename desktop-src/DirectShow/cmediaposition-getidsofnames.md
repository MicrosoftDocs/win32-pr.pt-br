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
ms.openlocfilehash: eebd32638afdf957024f54f6a601e95bae274dc4ab9a8265e9a618d635a23530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634786"
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
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memória insuficiente.<br/>                     |
| <dl> <dt>**Não receber \_ E não \_ conhecido**</dt> </dl> | Um ou mais dos nomes não eram conhecidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




