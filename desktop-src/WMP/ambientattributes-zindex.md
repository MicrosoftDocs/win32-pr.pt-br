---
title: Ambienteattributes. zIndex
description: O atributo zIndex especifica ou recupera a ordem na qual o controle é renderizado.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- ZIndex do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770527"
---
# <a name="ambientattributeszindex"></a>Ambienteattributes. zIndex

O atributo **ZIndex** especifica ou recupera a ordem na qual o controle é renderizado.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) com um valor padrão de zero. O intervalo é o de um inteiro longo assinado.

## <a name="remarks"></a>Comentários

O bitmap em segundo plano de uma **exibição** ou **subexibição** tem um índice z fixo de zero. Se você quiser que um controle esteja por trás do plano de fundo, o **ZIndex** deverá ser definido como um número negativo.

O índice z de um **modo de exibição** ou de uma **subexibição** é um índice absoluto, enquanto o índice z de um controle é relativo ao índice z da **exibição** ou **subexibição** que o contém.

Não há suporte para o atributo **ZIndex** nos elementos **browser** e **playlist** . Ele não funcionará com o elemento **Video** se for um *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver **efeitos**. em **janela** é definido como true.

Os elementos **buttonelement** usam o **ZIndex** de seus **botões**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





