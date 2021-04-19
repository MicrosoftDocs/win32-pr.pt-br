---
title: BOTÃO de fundo.
description: O atributo de exibição de fundo especifica ou recupera um valor que indica se o myButton exibe apenas os botões ou exibe o bitmap completo especificado no atributo Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- The. para o Windows Media Player em segundo plano
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796440"
---
# <a name="buttongroupshowbackground"></a>BOTÃO de fundo.

O atributo de exibição de **fundo** especifica ou recupera um valor que indica se o **MyButton** exibe apenas os botões ou exibe o bitmap completo especificado no atributo **Image** .

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Os botões são exibidos e a área não ocupada pelos botões é desenhada a partir do bitmap de imagem. |
| false | Padrão. Somente os botões são exibidos.                                                   |



 

## <a name="remarks"></a>Comentários

Quando o modo de **fundo** for true, toda a **imagem** principal ficará visível.

Quando a cor do **plano de fundo** for falsa, somente as áreas correspondentes às cores **mappingImage** atribuídas serão renderizadas. Em outras palavras, somente **BUTTONELEMENTs** com seus **mappingColor** atribuídos estarão visíveis.

Se um valor inválido for especificado, o estado anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**BUTTONelement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTON. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTON. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





