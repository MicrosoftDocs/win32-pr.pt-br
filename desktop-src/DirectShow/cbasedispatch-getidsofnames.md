---
description: Método CBaseDispatch. GetIDsOfNames – o método GetIDsOfNames mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Método CBaseDispatch. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9153dd2412018321374f558539690d5d146d8547d6247874bf5c1c79f1d4d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660023"
---
# <a name="cbasedispatchgetidsofnames-method"></a>Método CBaseDispatch. GetIDsOfNames

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

Referência a um IID (identificador de interface) que especifica a interface.

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



 

## <a name="remarks"></a>Comentários

Esse método se comporta como o método **IDispatch:: GetIDsOfNames** , mas o parâmetro *riid* especifica a interface na qual recuperar DISPIDs. (Na versão **IDispatch** , o parâmetro *riid* é reservado.)

Se o método retornar \_ e não \_ conhecido, os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




