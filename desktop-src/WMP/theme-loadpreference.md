---
title: THEME. loadpreference
description: O método loadpreference carrega uma preferência do registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME. loadpreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782220"
---
# <a name="themeloadpreference"></a>THEME. loadpreference

O método **loadpreference** carrega uma preferência do registro.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Uma **cadeia de caracteres** que especifica a chave do valor de preferência a ser carregado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Uma preferência é um par chave/valor que pode ser armazenado no registro para reter informações sobre o estado do Windows Media Player entre execuções. Esse recurso pode ser usado, por exemplo, para salvar configurações de personalização para que elas não precisem ser reinseridas sempre que o Windows Media Player for iniciado.

As preferências não são criptografadas e, portanto, não são um método seguro para persistir dados. Não use as preferências para armazenar dados privados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





