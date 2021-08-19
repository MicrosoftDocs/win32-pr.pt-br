---
title: Atributo WM/UniqueFileIdentifier
description: O atributo WM/UniqueFileIdentifier é uma cadeia de caracteres que identifica exclusivamente o item.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Windows Media Player do atributo WM/UniqueFileIdentifier
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf29b5f4a0c2bf6e2642ce13f190a4734a2fb4ff395481b1ba93bc5feeb6db89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930812"
---
# <a name="wmuniquefileidentifier-attribute"></a>Atributo WM/UniqueFileIdentifier

O atributo **WM/UniqueFileIdentifier** é uma cadeia de caracteres que identifica exclusivamente o item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**UniqueFileIdentifier** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMUniqueFileIdentifier.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





