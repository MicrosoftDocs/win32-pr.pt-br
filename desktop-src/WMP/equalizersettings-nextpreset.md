---
title: EQUALIZERSETTINGS.nextPreset
description: O método nextPreset aplica a próxima predefinição de equalizador.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761097"
---
# <a name="equalizersettingsnextpreset"></a>EQUALIZERSETTINGS.nextPreset

O método **nextPreset** aplica a próxima predefinição de equalizador.

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a predefinição atual for a última disponível, a primeira predefinição será tornada atual.

## <a name="examples"></a>Exemplos


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.previousPreset**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





