---
title: Atributo do WM/year
description: O atributo WM/year é o ano em que o conteúdo foi publicado.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Atributo do WM/year do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749552"
---
# <a name="wmyear-attribute"></a>Atributo do WM/year

O atributo **WM/year** é o ano em que o conteúdo foi publicado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente no arquivo de mídia digital.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

Esse atributo não deve ser usado como parte de uma condição de consulta. Ele é derivado de outro atributo e não pode ser consultado diretamente em uma coleção de mídia.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMYear.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versão<br/> | O Windows Media Player 9 Series Windows Media Player 10 ou posterior não oferece suporte a esse atributo<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





