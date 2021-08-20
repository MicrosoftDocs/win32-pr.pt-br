---
title: BOTÃO de fundo.
description: O atributo de exibição de fundo especifica ou recupera um valor que indica se o myButton exibe apenas os botões ou exibe o bitmap completo especificado no atributo Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- Windows Media Player de botão. tudo em segundo plano
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342669"
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

 

 





