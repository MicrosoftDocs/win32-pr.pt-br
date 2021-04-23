---
description: O elemento Effect define um objeto de efeito de áudio ou vídeo. Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908653"
---
# <a name="effect-element"></a>Elemento Effect

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `effect` elemento define um objeto de efeito de áudio ou vídeo. Um efeito é aplicado a um único fluxo (como uma composição, faixa ou origem).

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**Bloquear**](lock-attribute.md), [**ativar mudo**](mute-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nome de usuário**](username-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



| Label | Valor |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Pai   | [**composto**](composite-element.md), [**Agrupar**](group-element.md), [**recortar**](clip-element.md), [**acompanhar**](track-element.md) |
| Children | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Comentários

O atributo **CLSID** especifica o subobjeto que cria o efeito.

## <a name="examples"></a>Exemplos


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Gdipluseffects. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




