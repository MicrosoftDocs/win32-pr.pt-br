---
title: Atributo WM/WMContentID
description: O atributo WM/WMContentID é um GUID que identifica o conteúdo do item.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- Atributo WM/WMContentID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760541"
---
# <a name="wmwmcontentid-attribute"></a>Atributo WM/WMContentID

O atributo **WM/WMContentID** é um GUID que identifica o conteúdo do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**WMContentID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





