---
title: Atributo WM/Language
description: O atributo WM/Language é o idioma do item.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Atributo WM/Language Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8902d36ebe9e8227d22f55273e8351d7ed09c592953b44a31e45c06b838f9871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122646"
---
# <a name="wmlanguage-attribute"></a>Atributo WM/Language

O **atributo WM/Language** é o idioma do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca e no arquivo de mídia digital.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com vários valores, você deve usar o método **Media.getItemInfoByType,** não o **método Media.getItemInfo.**

**Language** é um alias para esse atributo.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMLanguage.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior (o item de rádio tem suporte apenas no Windows Media Player série 9)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





