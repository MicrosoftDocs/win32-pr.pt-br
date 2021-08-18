---
description: 'O método Help invoca a ajuda da página de propriedades. Esse método implementa o método IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Método CBasePropertyPage. Help (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955085"
---
# <a name="cbasepropertypagehelp-method"></a>Método CBasePropertyPage. Help

O `Help` método invoca a ajuda da página de propriedades. Esse método implementa o método **IPropertyPage:: help** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

Ponteiro para a cadeia de caracteres sob a chave **HelpDir** nas informações de CLSID da página de propriedades no registro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Na classe base, o método sempre retorna E \_ NOTIMPL. Quando o método falha, o quadro chama **IPropertyPage:: GetPageInfo** para obter o nome do arquivo de ajuda e o identificador de contexto. Por padrão, elas são **nulas**. Para fornecer ajuda, portanto, a classe derivada pode substituir o método `Help` ou o método [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




