---
description: O método CheckMediaType determina se um tipo de mídia proposto é compatível com o formato de exibição.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Método CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749620"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Método CImageDisplay. CheckMediaType

O `CheckMediaType` método determina se um tipo de mídia proposto é compatível com o formato de exibição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pmtIn* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>       | Tipo de mídia inválido.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Tipo de mídia inválido.<br/>           |
| <dl> <dt>**S \_ OK**</dt> </dl>         | O tipo de mídia é compatível.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




