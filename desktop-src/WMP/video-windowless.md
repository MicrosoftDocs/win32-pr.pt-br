---
title: VÍDEO. sem janela
description: O atributo sem janela especifica ou recupera um valor que indica se o controle de vídeo será em janelas ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VÍDEO. Windows Media Player sem janela
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763937"
---
# <a name="videowindowless"></a>VÍDEO. sem janela

O atributo **sem janela** especifica ou recupera um valor que indica se o controle de vídeo será em janelas ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado. Só pode ser definido em tempo de design.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** especificado em tempo de design e somente leitura depois.



| Valor | Descrição                              |
|-------|------------------------------------------|
| true  | O controle de vídeo não terá janela.        |
| false | Padrão. O controle de vídeo será janelas. |



 

## <a name="remarks"></a>Comentários

Se uma janela de vídeo não retangular for desejada ou se você quiser cobrir qualquer parte da janela de vídeo com uma imagem, esse atributo deverá ser definido como true. Isso sacrificaria algum desempenho para fazer o recorte necessário.

A reprodução de vídeo é otimizada para reprodução não recortada. Nesse caso, o atributo **sem janela** é definido como false e todo o retângulo de vídeo é sempre exibido. Qualquer imagem que abranja a janela de vídeo é ignorada e a janela de vídeo tem a ordem z de nível mais alto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





