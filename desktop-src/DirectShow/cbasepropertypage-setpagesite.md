---
description: 'O método SetPageSite Inicializa a página de propriedades e fornece um ponteiro para a interface IPropertyPageSite do quadro de propriedades. Esse método implementa o método IPropertyPage:: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Método CBasePropertyPage. SetPageSite (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755606"
---
# <a name="cbasepropertypagesetpagesite-method"></a>Método CBasePropertyPage. SetPageSite

O `SetPageSite` método inicializa a página de propriedades e fornece um ponteiro para a interface **IPropertyPageSite** do quadro de propriedades. Esse método implementa o método **IPropertyPage:: SetPageSite** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPageSite* 
</dt> <dd>

Ponteiro para a interface **IPropertyPageSite** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/> |



 

## <a name="remarks"></a>Comentários

O método armazena o ponteiro *pPageSite* na variável de membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




