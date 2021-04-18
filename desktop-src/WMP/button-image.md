---
title: BOTÃO. imagem
description: O atributo Image especifica ou recupera a imagem padrão do botão.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. Image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763369"
---
# <a name="buttonimage"></a>BOTÃO. imagem

O atributo **Image** especifica ou recupera a imagem padrão do **botão**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (incluindo GIFs animados).

Se a imagem do **botão** for maior do que a região definida pelos atributos **Width** e **Height** , a imagem será cortada.

Se a imagem não for especificada, mas a **altura** e a **largura** forem, a imagem diretamente atrás desse controle será exibida. Isso pode facilitar o desenho da imagem na própria **exibição** , reduzindo o número de arquivos de imagem separados necessários.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





