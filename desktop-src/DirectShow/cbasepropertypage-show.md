---
description: 'O método Show mostra ou oculta a caixa de diálogo. Esse método implementa o método IPropertyPage:: show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Método CBasePropertyPage. show (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754557"
---
# <a name="cbasepropertypageshow-method"></a>Método CBasePropertyPage. show

O `Show` método mostra ou oculta a caixa de diálogo. Esse método implementa o método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="syntax"></a>Sintaxe

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Parâmetros

*nCmdShow*

Tipo: **[uint](../winprog/windows-data-types.md)**

Valor que especifica se a janela deve ser mostrada ou ocultada. Para obter mais informações, consulte o método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.

| Código de retorno                                                                                  | Descrição                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/>   |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |

## <a name="see-also"></a>Confira também

[Classe CBasePropertyPage](cbasepropertypage.md)
