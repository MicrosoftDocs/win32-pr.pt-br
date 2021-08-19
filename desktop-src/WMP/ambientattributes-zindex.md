---
title: AmbientAttributes.zIndex
description: O atributo zIndex especifica ou recupera a ordem na qual o controle é renderizado.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbienteAttributes.zIndex Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0ebccb050d80371b5865316dd341c8e371d3bfd399d14545b312cf8d265bac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124036"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes.zIndex

O **atributo zIndex** especifica ou recupera a ordem na qual o controle é renderizado.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um  número de leitura/gravação (**longo**) com um valor padrão de zero. O intervalo é o de um inteiro longo com sinal.

## <a name="remarks"></a>Comentários

O bitmap em segundo plano de **um VIEW** ou **SUBVIEW** tem um índice z fixo de zero. Se você quiser que um controle seja o segundo plano, **o zIndex** deverá ser definido como um número negativo.

O índice z de **uma VIEW** ou **SUBVIEW** é um índice absoluto, enquanto o índice z de um controle é relativo ao índice z da **VIEW** ou **SUBVIEW** que o contém.

O **atributo zIndex** não é suportado pelos elementos **BROWSER** e **PLAYLIST.** Ele não funcionará com o elemento **VIDEO** se *VIDEO*. **windowless é** definido como false, nem com o elemento **EFFECTS** se **EFFECTS**. **windowed** é definido como true.

**Os elementos BUTTONELEMENT** usam **o zIndex** de **seu BUTTONGROUP.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





