---
title: WMPEFFECTS
description: Isso é um efeito predefinido com os valores padrão a seguir.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Windows Media Player
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793852"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Isso é um **efeito** predefinido com os valores padrão a seguir.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Comentários

Isso criará um elemento **Effects** que irá percorrer as predefinições de visualização quando o usuário clicar no controle. Ele também irá ampliar as visualizações quando o player for redimensionado.

A predefinição de visualização inicial mostrada é aquela selecionada no menu **Exibir** em **visualizações**. Alterar a seleção nesse menu alterará automaticamente a predefinição exibida por esse elemento quando o Player estiver no modo de capa. O menu **Exibir** é exibido no modo completo do Player ou quando o atributo **View. TitleBar** é definido como true em uma capa.

Todas as propriedades desse elemento **Effects** podem ser substituídas especificando-as explicitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> </dl>

 

 





