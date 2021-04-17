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
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811756"
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

## <a name="return-value"></a>Retornar valor

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Na classe base, o método sempre retorna E \_ NOTIMPL. Quando o método falha, o quadro chama **IPropertyPage:: GetPageInfo** para obter o nome do arquivo de ajuda e o identificador de contexto. Por padrão, elas são **nulas**. Para fornecer ajuda, portanto, a classe derivada pode substituir o método `Help` ou o método [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




