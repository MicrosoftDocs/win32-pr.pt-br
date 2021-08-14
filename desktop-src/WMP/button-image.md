---
title: BUTTON.image
description: O atributo de imagem especifica ou recupera a imagem padrão do BUTTON.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON.image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85874c79db8f3174b70af68c3ff1e58511c3f00cc7d648389dbca971c7efd96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342904"
---
# <a name="buttonimage"></a>BUTTON.image

O **atributo** de imagem especifica ou recupera a imagem padrão do **BUTTON.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (incluindo GIFs animados).

Se a **imagem BUTTON** for maior que  a região definida pelos atributos **de** largura e altura, a imagem será cortada.

Se a imagem não for especificada, mas a **altura** e **a largura,** a imagem diretamente atrás desse controle será exibida. Isso pode facilitar o desenho da imagem no **próprio VIEW,** reduzindo o número de arquivos de imagem separados necessários.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem x vermelha) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





