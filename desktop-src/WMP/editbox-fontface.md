---
title: EDITBOX.fontFace
description: O atributo fontFace especifica ou recupera a fonte para texto no controle de caixa de edição.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EDITBOX.fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3994c9cef1f645dc9c1129876b9144471caf9f608f5911641b180deae437194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996856"
---
# <a name="editboxfontface"></a>EDITBOX.fontFace

O **atributo fontFace** especifica ou recupera a fonte do texto no controle de caixa de edição.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows. Windows Media Player não dará suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.

Se **o fontFace** especificado não estiver disponível no sistema do usuário, o controle de caixa de edição assume como padrão a fonte Windows sistema. O valor padrão para sistemas de idioma inglês é "Tahoma". Para sistemas internacionais, o padrão é carregado de um arquivo de recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX.fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





