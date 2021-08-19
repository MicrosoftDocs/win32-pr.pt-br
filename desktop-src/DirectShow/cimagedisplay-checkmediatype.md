---
description: O método CheckMediaType determina se um tipo de mídia proposto é compatível com o formato de exibição.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Método CImageDisplay.CheckMediaType (Winutil.h)
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
ms.openlocfilehash: 6bad6a7242ba110ad3916d08070eef40a8fa1d5d658ea366732e14a1cd107d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087386"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Método CImageDisplay.CheckMediaType

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

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que contém o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Tipo de mídia inválido.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Tipo de mídia inválido.<br/>           |
| <dl> <dt>**S \_ OK**</dt> </dl>         | O tipo de mídia é compatível.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




