---
title: Atributo WM/Year
description: O atributo WM/Year é o ano em que o conteúdo foi publicado.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Atributo WM/Year Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900186"
---
# <a name="wmyear-attribute"></a>Atributo WM/Year

O **atributo WM/Year** é o ano em que o conteúdo foi publicado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no arquivo de mídia digital.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

Esse atributo não deve ser usado como parte de uma condição de consulta. Ele é derivado de outro atributo e não pode ser consultado diretamente em uma coleção de mídias.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMYear.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 Windows Media Player 10 ou posterior não dá suporte a esse atributo<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





