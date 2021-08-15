---
title: BUTTONGROUP.showBackground
description: O atributo showBackground especifica ou recupera um valor que indica se BUTTONGROUP exibe apenas os botões ou exibe o bitmap completo especificado no atributo de imagem.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP.showBackground Windows Media Player
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
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

O **atributo showBackground** especifica ou recupera um valor que indica se **BUTTONGROUP** exibe apenas os botões ou exibe o bitmap completo especificado no atributo **de** imagem.

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Os botões são exibidos e a área não ocupada pelos botões é desenhada do bitmap de imagem. |
| false | Padrão. Somente os botões são exibidos.                                                   |



 

## <a name="remarks"></a>Comentários

Quando **showBackground** for true, toda a imagem **principal** ficará visível.

Quando **showBackground** for false, somente as áreas correspondentes ao **mapeamento atribuídoImagem** de cores serão renderizadas. Em outras palavras, somente **BUTTONELEMENTs** com **seu mappingColor** atribuído ficará visível.

Se um valor inválido for especificado, o estado anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





