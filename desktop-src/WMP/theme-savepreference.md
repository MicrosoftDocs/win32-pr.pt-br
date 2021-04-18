---
title: THEME. savePreference
description: O método savePreference salva uma preferência no registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME. savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780249"
---
# <a name="themesavepreference"></a>THEME. savePreference

O método **savePreference** salva uma preferência no registro.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Uma **cadeia de caracteres** que especifica a chave do valor de preferência a ser salvo.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*o valor*
</dt> <dd>

Uma **cadeia de caracteres** que especifica o valor a ser salvo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Uma preferência é um par chave/valor que pode ser armazenado no registro para reter informações sobre o estado do Windows Media Player entre execuções. Esse recurso pode ser usado, por exemplo, para salvar configurações de personalização para que elas não precisem ser reinseridas sempre que o Windows Media Player for iniciado.

As preferências não são criptografadas e, portanto, não são um método seguro para persistir dados. Não use as preferências para armazenar dados privados.

## <a name="examples"></a>Exemplos


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. loadpreference**](theme-loadpreference.md)
</dt> </dl>

 

 





