---
title: THEME.savePreference
description: O método savePreference salva uma preferência no Registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME.savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5f9edca154ff6402028ba873c1643e330ab316a54a63f14fa4f9b5bdb244483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134539"
---
# <a name="themesavepreference"></a>THEME.savePreference

O **método savePreference** salva uma preferência no Registro.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Uma **Cadeia de** caracteres que especifica a chave do valor de preferência a ser salvo.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*
</dt> <dd>

Uma **Cadeia de** caracteres que especifica o valor a ser salvo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Uma preferência é um par chave-valor que pode ser armazenado no Registro para reter informações sobre o estado de Windows Media Player entre as executações. Esse recurso pode ser usado, por exemplo, para salvar as configurações de personalização para que elas não tenham que ser inseridas de novo sempre que Windows Media Player é iniciada.

As preferências não são criptografadas e, portanto, não são um método seguro para persistir dados. Não use preferências para armazenar dados privados.

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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





