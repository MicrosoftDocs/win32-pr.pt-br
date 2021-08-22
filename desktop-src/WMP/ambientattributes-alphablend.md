---
title: Ambienteattributes. alphaBlend
description: O atributo alphaBlend especifica ou recupera um valor para a mistura alfa de qualquer exibição, subexibição ou widget de interface do usuário.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Windows Media Player ambientalattributes. alphaBlend
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b7170931c8fc266fdc335076dbc6dc687795f9bb432518b62a39d1f610b601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391706"
---
# <a name="ambientattributesalphablend"></a>Ambienteattributes. alphaBlend

O atributo **alphaBlend** especifica ou recupera um valor para a mistura alfa de qualquer **exibição**, **subexibição** ou widget de interface do usuário.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) com um valor que varia de 0 (sem opacidade) a 255 (opacidade total) e um valor padrão de 255.

## <a name="remarks"></a>Comentários

Esse atributo permite que um elemento apareça semitransparente, dependendo da quantidade de opacidade definida. Quanto menor a opacidade, mais transparente será a aparência do elemento. Cada elemento na capa pode ter um valor de opacidade separado, exceto os elementos de botão em um controle de **botão** . Quando **alphaBlend** é definido na **exibição**, a opacidade de toda a capa será definida. O Alpha Blend não funcionará para controles em janela, incluindo **playlist**, **Effects**, **ListBox**,  **Popup**, e **Video** (se **sem janelas** estiver definido como false). Quando **alphaBlend** é definido na **exibição**, toda a capa torna-se transparente. Os atributos **transparencyColor** usados por vários elementos não têm suporte com **alphaBlend**.

Quando você usa **alphaBlend** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para *texto*.**foregroundColor**), seu texto pode se tornar ilegível. Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.

> [!Note]  
> não há suporte para esse atributo no Windows 98.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





